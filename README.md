# LCTF2017_Dr.HuaJi_- 滑稽博士
A solution and writeup. https://github.com/LCTF/LCTF2017/tree/master/src/re/%E6%BB%91%E7%A8%BD%E5%8D%9A%E5%A3%AB

Solution

The function to generate Player and Huaji can be found in the mainp.

Step into these functions, we can easily find that the structure
recording the HP,MAX HP, MP and MAX MP of HuaJi is at 9C30 (RAW) ,and
9C40 for the player.

Just change the HP of HuaJi to 01 00 (=1) with a hex editor. Then you
can easily kill HuaJi in the game for 10 times and finally you can get
the flag.

Be careful about the change to the structures mentiond above, because
the generating process of flag is related to the MAX HP，MP and MAX MP
of HuaJi and the player , so that any change to these value will make
the flag unreadable.
