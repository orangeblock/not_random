This is a demonstration how to rebuild the internal state of a Mersenne Twister by using only parts of its output. In this example it uses 8 bits per 64 bit MT-output.

For details see https://spideroak.com/blog/20121205114003-exploit-information-leaks-in-random-numbers-from-python-ruby-and-php

The Mersenne Twister implementation is in twister.py. The script `gen_magic_data.py` precalculates the
`magic_data`. (This may take a while, so `magic_data` is already included.)

rebuild_random.py demonstrates that it works.

Boring output of the rebuild_random.py:

```
$ python ./rebuild_random.py 
Loading Magic
Done.
Working.... I need 3115 bytes from MT
BBBBBBBBBBBBBBBBBBBBBBBBBBBDDDDCCCCCCCCCCCCCEEEDDDDEEGFHJSREOIHFEEDDEEECCCCCCCBB
BBBBBBBBBBBBBBBBBBBBBBBBBBCDDDDDDCCCCCCCCCDDEEEEFFEEFGRQQF..ONCJFFEEEEDDCCCCCCCC
BBBBBBBBBBBBBBBBBBBBBBBBBCCDDDDDDDDEEDDDDDDDFEEEFFFGGGIRI.....PIGGFEEEFDDDDEDDDD
BBBBBBBBBBBBBBBBBBBBBBBBCCCDDDDDDDDDEEEDDDDEGFGGGHGHHIJO......RJHIGGFFFEFEEDDDDD
CCCBBBBBBBBBBBBBBBBBBCCCCCCDDDDDDDDDEEEEEFFGGNRTKJICBOLBTM..IAQOPMNJIGHHPIEDDDDD
CCCCCCCCCCBBBBBBBCCCCCCCCCDEDDDDDDDDEEEEEFFFGLP..TDK..............HPLMEAPTGEEEEC
CCCCCCCCCCCCDDDDCCCCCCCCCDDEEEDDDDDFFEEEEFGGHKQ.........................NJFFEDDC
CCCCCCCCCCCCCDDDDDDDEDDDDDFEEEFEEEEFFFGGFGIMRN........................JPJGGEEDDC
CCCCCCCCCCCCCDDDDDDDDEEEFFKIGFFGGFGFFFGGGIJO............................TIIGFFDD
CCCCCCCCCCCCCCDDDDDDDEEEEFKKIIHHJBIHGIHHHIF.............................G.QJFEEE
BCCCCCCCCCCCCCDDDDDDDEFFFGHJNNOLMPJLRJIJILI..............................QJGGEDD
BBCCCCCCCCCCCDEEDDDDDEFFFGHIFP.L.....DDMMO...............................HLGGDDD
BBBDDDCCCCCCDDEEEEFFEFHGHIRRA...........PA...............................JJFEEED
BBBCDDDDEEDDDFEEEEFFHGJKKKME.............K...............................LHGEEEE
BBBBCDDDFEEFIFFGFGGHHJKPT.P.............................................QGGFEDDD
BBBBCC................................................................PJHGFEEDDD
BBBBCDDDFEEFIFFGFGGHHJKPT.P.............................................QGGFEDDD
BBBCDDDDEEDDDFEEEEFFHGJKKKME.............K...............................LHGEEEE
BBBDDDCCCCCCDDEEEEFFEFHGHIRRA...........PA...............................JJFEEED
BBCCCCCCCCCCCDEEDDDDDEFFFGHIFP.L.....DDMMO...............................HLGGDDD
BCCCCCCCCCCCCCDDDDDDDEFFFGHJNNOLMPJLRJIJILI..............................QJGGEDD
CCCCCCCCCCCCCCDDDDDDDEEEEFKKIIHHJBIHGIHHHIF.............................G.QJFEEE
CCCCCCCCCCCCCDDDDDDDDEEEFFKIGFFGGFGFFFGGGIJO............................TIIGFFDD
CCCCCCCCCCCCCDDDDDDDEDDDDDFEEEFEEEEFFFGGFGIMRN........................JPJGGEEDDC
CCCCCCCCCCCCDDDDCCCCCCCCCDDEEEDDDDDFFEEEEFGGHKQ.........................NJFFEDDC
CCCCCCCCCCBBBBBBBCCCCCCCCCDEDDDDDDDDEEEEEFFFGLP..TDK..............HPLMEAPTGEEEEC
CCCBBBBBBBBBBBBBBBBBBCCCCCCDDDDDDDDDEEEEEFFGGNRTKJICBOLBTM..IAQOPMNJIGHHPIEDDDDD
BBBBBBBBBBBBBBBBBBBBBBBBCCCDDDDDDDDDEEEDDDDEGFGGGHGHHIJO......RJHIGGFFFEFEEDDDDD
BBBBBBBBBBBBBBBBBBBBBBBBBCCDDDDDDDDEEDDDDDDDFEEEFFFGGGIRI.....PIGGFEEEFDDDDEDDDD
BBBBBBBBBBBBBBBBBBBBBBBBBBCDDDDDDCCCCCCCCCDDEEEEFFEEFGRQQF..ONCJFFEEEEDDCCCCCCCC
BBBBBBBBBBBBBBBBBBBBBBBBBBBDDDDCCCCCCCCCCCCCEEEDDDDEEGFHJSREOIHFEEDDEEECCCCCCCBB
RANDOM POOL SUCCESSFULLY REBUILT!
```

Frank Sievertsen
@fx5
