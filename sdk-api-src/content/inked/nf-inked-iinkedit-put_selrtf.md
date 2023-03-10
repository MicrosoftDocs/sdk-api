---
UID: NF:inked.IInkEdit.put_SelRTF
title: IInkEdit::put_SelRTF (inked.h)
description: Gets or sets the currently selected Rich Text Format (RTF) formatted text in the InkEdit control (run time only). (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelRTF property","IInkEdit.SelRTF","IInkEdit.put_SelRTF","IInkEdit::SelRTF","IInkEdit::get_SelRTF","IInkEdit::put_SelRTF","InkEdit.get_SelRTF","InkEdit.put_SelRTF","SelRTF property [Tablet PC]","SelRTF property [Tablet PC]","IInkEdit interface","get_SelRTF","inked/IInkEdit::SelRTF","inked/IInkEdit::get_SelRTF","inked/IInkEdit::put_SelRTF","put_SelRTF","tablet.inkedit_selrtf"]
old-location: tablet\inkedit_selrtf.htm
tech.root: tablet
ms.assetid: 85dc3b6d-54fa-4f23-9d36-03becff886cf
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelRTF property, IInkEdit.SelRTF, IInkEdit.put_SelRTF, IInkEdit::SelRTF, IInkEdit::get_SelRTF, IInkEdit::put_SelRTF, InkEdit.get_SelRTF, InkEdit.put_SelRTF, SelRTF property [Tablet PC], SelRTF property [Tablet PC],IInkEdit interface, get_SelRTF, inked/IInkEdit::SelRTF, inked/IInkEdit::get_SelRTF, inked/IInkEdit::put_SelRTF, put_SelRTF, tablet.inkedit_selrtf
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkEdit::put_SelRTF
 - inked/IInkEdit::put_SelRTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.SelRTF
 - IInkEdit.get_SelRTF
 - IInkEdit.put_SelRTF
 - InkEdit.get_SelRTF
 - InkEdit.put_SelRTF
---

# IInkEdit::put_SelRTF


## -description

Gets or sets the currently selected Rich Text Format (RTF) formatted text in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

This property is read/write.

## -parameters

## -remarks

Setting the SelRTF property replaces any selected text in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control with the new string. This property returns a zero-length string ("") if no text is selected in the control.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
