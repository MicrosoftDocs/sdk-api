---
UID: NF:inked.IInkEdit.put_SelItalic
title: IInkEdit::put_SelItalic
author: windows-sdk-content
description: Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is italic (run time only).
old-location: tablet\inkedit_selitalic.htm
tech.root: tablet
ms.assetid: ea6f6495-d740-4aad-8310-7ce43f36cd93
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IInkEdit interface [Tablet PC],SelItalic property, IInkEdit.SelItalic, IInkEdit.put_SelItalic, IInkEdit::SelItalic, IInkEdit::get_SelItalic, IInkEdit::put_SelItalic, InkEdit.get_SelItalic, InkEdit.put_SelItalic, SelItalic property [Tablet PC], SelItalic property [Tablet PC],IInkEdit interface, get_SelItalic, inked/IInkEdit::SelItalic, inked/IInkEdit::get_SelItalic, inked/IInkEdit::put_SelItalic, put_SelItalic, tablet.inkedit_selitalic
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
 - IInkEdit.SelItalic
 - IInkEdit.get_SelItalic
 - IInkEdit.put_SelItalic
 - InkEdit.get_SelItalic
 - InkEdit.put_SelItalic
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
- IInkEdit.put_SelItalic
: 
---

# IInkEdit::put_SelItalic


## -description


Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control is italic (run time only).

This property is read/write.


## -parameters


## -remarks



If a selection spans multiple italicized and un-italicized characters, the <b>SelItalic</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control, setting this property indicates all new text entered at the current insertion point will be italicized.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

