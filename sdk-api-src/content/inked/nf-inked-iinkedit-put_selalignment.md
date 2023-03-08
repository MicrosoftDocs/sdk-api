---
UID: NF:inked.IInkEdit.put_SelAlignment
title: IInkEdit::put_SelAlignment (inked.h)
description: Gets or sets a value that controls the alignment of the paragraphs in an InkEdit control. (Put)
helpviewer_keywords: ["0","1","2","IInkEdit interface [Tablet PC]","SelAlignment property","IInkEdit.SelAlignment","IInkEdit.put_SelAlignment","IInkEdit::SelAlignment","IInkEdit::get_SelAlignment","IInkEdit::put_SelAlignment","InkEdit.get_SelAlignment","InkEdit.put_SelAlignment","NULL","SelAlignment property [Tablet PC]","SelAlignment property [Tablet PC]","IInkEdit interface","get_SelAlignment","inked/IInkEdit::SelAlignment","inked/IInkEdit::get_SelAlignment","inked/IInkEdit::put_SelAlignment","put_SelAlignment","tablet.inkedit_selalignment"]
old-location: tablet\inkedit_selalignment.htm
tech.root: tablet
ms.assetid: 62755220-b8e4-4f26-b5f4-8a1b4b7adc01
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, IInkEdit interface [Tablet PC],SelAlignment property, IInkEdit.SelAlignment, IInkEdit.put_SelAlignment, IInkEdit::SelAlignment, IInkEdit::get_SelAlignment, IInkEdit::put_SelAlignment, InkEdit.get_SelAlignment, InkEdit.put_SelAlignment, NULL, SelAlignment property [Tablet PC], SelAlignment property [Tablet PC],IInkEdit interface, get_SelAlignment, inked/IInkEdit::SelAlignment, inked/IInkEdit::get_SelAlignment, inked/IInkEdit::put_SelAlignment, put_SelAlignment, tablet.inkedit_selalignment
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
 - IInkEdit::put_SelAlignment
 - inked/IInkEdit::put_SelAlignment
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
 - IInkEdit.SelAlignment
 - IInkEdit.get_SelAlignment
 - IInkEdit.put_SelAlignment
 - InkEdit.get_SelAlignment
 - InkEdit.put_SelAlignment
---

# IInkEdit::put_SelAlignment


## -description

Gets or sets a value that controls the alignment of the paragraphs in an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

This property is read/write.

## -parameters

## -remarks

The <b>SelAlignment</b> property determines paragraph alignment for all paragraphs that have text in the current selection or for the paragraph containing the insertion point if no text is selected.

If a selection spans multiple paragraphs with different alignment styles, the <b>SelAlignment</b> property will be null.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
