1.first trick is yank all line at any position of the target line =>
    yy [i just can't get how it works,try it];also ,you can try y$,but this require the curser position at the start of the line.
2.yank the whole file =>
    you can press gg to locate your curser to the start of the file,then press yG to copy all the content from the start to end(G located) to buffer.
    the SV(shirt for stackoverflow) question url here:http://stackoverflow.com/questions/1620018/vi-editor-copy-all-the-lines-to-clipboard/19832192#19832192
3.P->paste before cursor,while p->paste after cursor
4.:x,ZZ or :wq->save and quit(:x->only save if necessary, ZZ->use it under normal mode)
5. .(dot)->will repeat the last command
6.N<command>->will repeat the command N times
7.word move:
    w->go to the start of the following word
    e->go to the end of this word
    PS:word definition:the obj composed of letters and the underscore characters
       WORD definition:a group of letter separated by blank characters
    W->go to the start of the following WORD
    E->go the end of this WORD
8.*->go to the next occurrence of the word under the cursot
  #->go to the prev occurrence of the word under the cursor
9.<start position><command><end position>
  e.g:0y$->yank the whole line content to buffer
10.gU/gu->make the letter(word) to Upper case or low case:w
11.killer movement:
    fa->go to the next occurrence of the letter "a" in cursor's line[';' will find the next oocurrence]
    ta->go to just before the letter "a" in cursor's line
    3fa->find the 3rd occurrence of the letter "a" in cursor's line
    dta->remove everything untill the letter "a" in cursor's line
    F and T->like f and t command but backward
12.zone selection:
    <action>a/i<object>:
        <action>:d/y/v/...
        <object>:w/W/s(sentence)/p(paragraph)/"/'/(/{/[/...
    PS:usage->vi)[chosen the inner part waped by ()]/va)[chosen the whole part as vi) and the wapper()]
       usage->v2i([chosen the second partion of the whole wappers]
13.select rectangular blocks:
   this commmand used to be comment action for mutiline code,e.g:^<c-v><jk for move><I//><esc> 
14.completion:
    <c-n>and<c-p> then magic happend!
15.macros:qa do sth q,@a,@@
    qa:record your action into register a
    @a:will replay the macro saved into the register a as if you typed it
    @@:is shortcut to replay the last executed macro
    PS:here is a example of how to quick insert 1-103 num into a file using macro[http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/]
16.visual selection:v,V,<c-v>
    usage:when you use block selection command to select a block,you can use:
        J(upper case j) to join all lines together
        <<(or >>) to indentto the left(right)
        = to auto indent
    usage:add sth on all seelcted lines ending
        <c-v>
        use j/<c-d>/%/... to the desired line
        $ go to the end of the line
        A
        wirte sth you want
        esc

PS:by the way,this blog is great in my personal opinion:http://yannesposito.com/
