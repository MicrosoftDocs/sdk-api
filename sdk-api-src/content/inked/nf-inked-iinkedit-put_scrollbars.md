---
UID: NF:inked.IInkEdit.put_ScrollBars
title: IInkEdit::put_ScrollBars
author: windows-sdk-content
description: Gets or sets the type of scroll bars, if any, to display in the InkEdit control.
old-location: tablet\inkedit_scrollbars.htm
tech.root: tablet
ms.assetid: d6b798dc-6e8f-4c89-b5a8-c4a189ebe6cd
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IInkEdit interface [Tablet PC],ScrollBars property, IInkEdit.ScrollBars, IInkEdit.put_ScrollBars, IInkEdit::ScrollBars, IInkEdit::get_ScrollBars, IInkEdit::put_ScrollBars, InkEdit.get_ScrollBars, InkEdit.put_ScrollBars, ScrollBars property [Tablet PC], ScrollBars property [Tablet PC],IInkEdit interface, get_ScrollBars, inked/IInkEdit::ScrollBars, inked/IInkEdit::get_ScrollBars, inked/IInkEdit::put_ScrollBars, put_ScrollBars, rtfBoth, rtfHorizontal, rtfNone, rtfVertical, tablet.inkedit_scrollbars
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
 - IInkEdit.ScrollBars
 - IInkEdit.get_ScrollBars
 - IInkEdit.put_ScrollBars
 - InkEdit.get_ScrollBars
 - InkEdit.put_ScrollBars
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit::put_ScrollBars


## -description


Gets or sets the type of scroll bars, if any, to display in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

This property is read/write.


## -parameters


## -remarks



For an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control with setting rtfHorizontal, rtfVertical, or rtfBoth, you must set the <a href="https://msdn.microsoft.com/361cfaea-d961-423c-98b0-f04bd7e621e9">MultiLine</a> property to <b>TRUE</b>.



At run time, the Windows operating environment automatically implements a standard keyboard interface to allow navigation in <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> controls with the arrow keys (UP ARROW, DOWN ARROW, LEFT ARROW, and RIGHT ARROW), the HOME and END keys, and so on.



Scroll bars are displayed only if the contents of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control extend beyond the control's borders. If <b>ScrollBars</b> is set to <b>FALSE</b>, the control won't have scroll bars, regardless of its contents.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

