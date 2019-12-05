---
UID: NF:inked.IInkEdit.get_MouseIcon
title: IInkEdit::get_MouseIcon (inked.h)
description: Gets or sets the custom mouse icon for the InkEdit control.
old-location: tablet\inkedit_mouseicon.htm
tech.root: tablet
ms.assetid: 11e7cf2d-e671-471f-9a13-1f55b62b4dfa
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],MouseIcon property, IInkEdit.MouseIcon, IInkEdit.get_MouseIcon, IInkEdit::MouseIcon, IInkEdit::get_MouseIcon, IInkEdit::put_MouseIcon, InkEdit.get_MouseIcon, InkEdit.put_MouseIcon, InkEdit.putref_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkEdit interface, get_MouseIcon, inked/IInkEdit::MouseIcon, inked/IInkEdit::get_MouseIcon, inked/IInkEdit::put_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkedit_mouseicon
ms.topic: method
f1_keywords:
- inked/IInkEdit.MouseIcon
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
- IInkEdit.MouseIcon
- IInkEdit.get_MouseIcon
- IInkEdit.put_MouseIcon
- InkEdit.get_MouseIcon
- InkEdit.put_MouseIcon
- InkEdit.putref_MouseIcon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::get_MouseIcon


## -description


Gets or sets the custom mouse icon for the
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

This property is read/write.


## -parameters


## -remarks



This property provides a custom icon that is used when the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer">MousePointer</a> property is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Custom</a>.

You can use the <b>MouseIcon</b> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

