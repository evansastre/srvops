# cp & mv

## cp

拷贝文件1到文件2，并保持文件的权限、属主和时间戳

```text
$ cp -p file1 file2
```

拷贝file1到file2，如果file2存在会提示是否覆盖

```text
$ cp -i file1 file2
```

```text
#copy file1 file2 to dir1
cp file1 file2 dir1
#copy dir1 dir2 to dir3
cp -r dir1 dir2 dir3

  -a或--archive 　此参数的效果和同时指定"-dpR"参数相同。 
　-b或--backup 　删除，覆盖目标文件之前的备份，备份文件会在字尾加上一个备份字符串。 
　-d或--no-dereference 　当复制符号连接时，把目标文件或目录也建立为符号连接，并指向与源文件或目录连接的原始文件或目录。 
　-f或--force 　强行复制文件或目录，不论目标文件或目录是否已存在。 
　-i或--interactive 　覆盖既有文件之前先询问用户。 
　-l或--link 　对源文件建立硬连接，而非复制文件。 
　-p或--preserve 　保留源文件或目录的属性。 
　-P或--parents 　保留源文件或目录的路径。 
　-r 　递归处理，将指定目录下的文件与子目录一并处理。 
　-R或--recursive 　递归处理，将指定目录下的所有文件与子目录一并处理。 
　-s或--symbolic-link 　对源文件建立符号连接，而非复制文件。 
　-S<备份字尾字符串>或--suffix=<备份字尾字符串> 　用"-b"参数备份目标文件后，备份文件的字尾会被加上一个备份字符串，预设的备份字尾字符串是符号"~"。 
　-u或--update 　使用这项参数后只会在源文件的更改时间较目标文件更新时或是　名称相互对应的目标文件并不存在，才复制文件。 
　-v或--verbose 　显示指令执行过程。 
　-V<备份方式>或--version-control=<备份方式> 　用"-b"参数备份目标文件后，备份文件的字尾会被加上一个备份字符串，这字符串不仅可用"-S"参数变更，当使用"-V"参数指定不同备份方式时，也会产生不同字尾的备份字串。  
　-x或--one-file-system 　复制的文件或目录存放的文件系统，必须与cp指令执行时所处的文件系统相同，否则不予复制。 
　--help 　在线帮助。 
　--sparse=<使用时机> 　设置保存稀疏文件的时机。 
　--version 　显示版本信息。
```

## mv

将文件名file1重命名为file2，如果file2存在则提示是否覆盖

```text
$ mv -i file1 file2
```

注意如果使用-f选项则不会进行提示

-v会输出重命名的过程，当文件名中包含通配符时，这个选项会非常方便

```text
$ mv -v file1 file2
```

