---
UID: NF:inked.IInkEdit.put_ScrollBars
title: IInkEdit::put_ScrollBars (inked.h)
description: Gets or sets the type of scroll bars, if any, to display in the InkEdit control.helpviewer_keywords: ["IInkEdit interface [Tablet PC]","ScrollBars property","IInkEdit.ScrollBars","IInkEdit.put_ScrollBars","IInkEdit::ScrollBars","IInkEdit::get_ScrollBars","IInkEdit::put_ScrollBars","InkEdit.get_ScrollBars","InkEdit.put_ScrollBars","ScrollBars property [Tablet PC]","ScrollBars property [Tablet PC]","IInkEdit interface","get_ScrollBars","inked/IInkEdit::ScrollBars","inked/IInkEdit::get_ScrollBars","inked/IInkEdit::put_ScrollBars","put_ScrollBars","rtfBoth","rtfHorizontal","rtfNone","rtfVertical","tablet.inkedit_scrollbars"]
old-location: tablet\inkedit_scrollbars.htm
tech.root: tablet
ms.assetid: d6b798dc-6e8f-4c89-b5a8-c4a189ebe6cd
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],ScrollBars property, IInkEdit.ScrollBars, IInkEdit.put_ScrollBars, IInkEdit::ScrollBars, IInkEdit::get_ScrollBars, IInkEdit::put_ScrollBars, InkEdit.get_ScrollBars, InkEdit.put_ScrollBars, ScrollBars property [Tablet PC], ScrollBars property [Tablet PC],IInkEdit interface, get_ScrollBars, inked/IInkEdit::ScrollBars, inked/IInkEdit::get_ScrollBars, inked/IInkEdit::put_ScrollBars, put_ScrollBars, rtfBoth, rtfHorizontal, rtfNone, rtfVertical, tablet.inkedit_scrollbars
f1_keywords:
- inked/IInkEdit.ScrollBars
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::put_ScrollBars


## -description


Gets or sets the type of scroll bars, if any, to display in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

This property is read/write.


## -parameters


## -remarks



For an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control with setting rtfHorizontal, rtfVertical, or rtfBoth, you must set the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline">MultiLine</a> property to <b>TRUE</b>.



At run time, the Windows operating environment automatically implements a standard keyboard interface to allow navigation in <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> controls with the arrow keys (UP ARROW, DOWN ARROW, LEFT ARROW, and RIGHT ARROW), the HOME and END keys, and so on.



Scroll bars are displayed only if the contents of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control extend beyond the control's borders. If <b>ScrollBars</b> is set to <b>FALSE</b>, the control won't have scroll bars, regardless of its contents.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

