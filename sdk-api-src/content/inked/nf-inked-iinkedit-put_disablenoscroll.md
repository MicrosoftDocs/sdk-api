---
UID: NF:inked.IInkEdit.put_DisableNoScroll
title: IInkEdit::put_DisableNoScroll
author: windows-sdk-content
description: Gets or sets a value that determines whether scroll bars in the InkEdit control are disabled.
old-location: tablet\inkedit_disablenoscroll.htm
tech.root: tablet
ms.assetid: 44a8372c-6323-4d76-9038-d61d210990b0
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DisableNoScroll property [Tablet PC], DisableNoScroll property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],DisableNoScroll property, IInkEdit.DisableNoScroll, IInkEdit.put_DisableNoScroll, IInkEdit::DisableNoScroll, IInkEdit::get_DisableNoScroll, IInkEdit::put_DisableNoScroll, InkEdit.get_DisableNoScroll, InkEdit.put_DisableNoScroll, get_DisableNoScroll, inked/IInkEdit::DisableNoScroll, inked/IInkEdit::get_DisableNoScroll, inked/IInkEdit::put_DisableNoScroll, put_DisableNoScroll, tablet.inkedit_disablenoscroll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkEd.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.DisableNoScroll
 - IInkEdit.get_DisableNoScroll
 - IInkEdit.put_DisableNoScroll
 - InkEdit.get_DisableNoScroll
 - InkEdit.put_DisableNoScroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit::put_DisableNoScroll


## -description


Gets or sets a value that determines whether scroll bars in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control are disabled.

This property is read/write.


## -parameters


## -remarks



The <b>DisableNoScroll</b> property is ignored when the <a href="https://msdn.microsoft.com/d6b798dc-6e8f-4c89-b5a8-c4a189ebe6cd">ScrollBars</a> property is set to <b>rtfNone</b>. However, when <b>ScrollBars</b> is set to <b>rtfHorizontal</b>, <b>rtfVertical</b>, or <b>rtfBoth</b>, individual scroll bars are disabled when there are too few lines of text to scroll vertically or too few characters of text to scroll horizontally in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.



This property is read-only at run time.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

