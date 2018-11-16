---
UID: NF:inked.IInkEdit.get_SelBold
title: IInkEdit::get_SelBold
author: windows-sdk-content
description: Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is bold.
old-location: tablet\inkedit_selbold.htm
tech.root: tablet
ms.assetid: 423f9303-38e9-4d70-88cd-e6503a9f0a64
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FALSE, IInkEdit interface [Tablet PC],SelBold property, IInkEdit.SelBold, IInkEdit.get_SelBold, IInkEdit::SelBold, IInkEdit::get_SelBold, IInkEdit::put_SelBold, InkEdit.get_SelBold, InkEdit.put_SelBold, NULL, SelBold property [Tablet PC], SelBold property [Tablet PC],IInkEdit interface, TRUE, get_SelBold, inked/IInkEdit::SelBold, inked/IInkEdit::get_SelBold, inked/IInkEdit::put_SelBold, put_SelBold, tablet.inkedit_selbold
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
 - IInkEdit.SelBold
 - IInkEdit.get_SelBold
 - IInkEdit.put_SelBold
 - InkEdit.get_SelBold
 - InkEdit.put_SelBold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- inked.h
: 
- IInkEdit.get_SelBold
: 
---

# IInkEdit::get_SelBold


## -description


Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control is bold.

This property is read/write.


## -parameters


## -remarks



If a selection spans multiple characters with different bold styles, the <b>SelBold</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control, setting this property determines whether all new text entered at the current insertion point is bold.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

