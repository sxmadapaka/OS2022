## 1.1 Hello OS

实验代码：

```assembly
	org 07c00h
	mov ax,cs
	mov ds,ax
	mov es,ax
	call	DispStr
	jmp $
DispStr:
	mov ax,BootMessage
	mov bp,ax
	mov cx,16
	mov ax,01301h
	mov bx,000ch
	mov dl,0
	int 10h
	ret
BootMessage:	db "Hello OS"
times 510-($-$$) db 0
dw 0xaa55
```

实验截图：

![ED0E0840914964851479D9C1A5815B82](/Users/wyh0111jx/Library/Containers/com.tencent.qq/Data/Library/Caches/Images/ED0E0840914964851479D9C1A5815B82.png)

