---
UID: NF:inked.IInkEdit.put_SelBold
title: IInkEdit::put_SelBold (inked.h)
description: Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is bold. (Put)
helpviewer_keywords: ["FALSE","IInkEdit interface [Tablet PC]","SelBold property","IInkEdit.SelBold","IInkEdit.put_SelBold","IInkEdit::SelBold","IInkEdit::get_SelBold","IInkEdit::put_SelBold","InkEdit.get_SelBold","InkEdit.put_SelBold","NULL","SelBold property [Tablet PC]","SelBold property [Tablet PC]","IInkEdit interface","TRUE","get_SelBold","inked/IInkEdit::SelBold","inked/IInkEdit::get_SelBold","inked/IInkEdit::put_SelBold","put_SelBold","tablet.inkedit_selbold"]
old-location: tablet\inkedit_selbold.htm
tech.root: tablet
ms.assetid: 423f9303-38e9-4d70-88cd-e6503a9f0a64
ms.date: 12/05/2018
ms.keywords: FALSE, IInkEdit interface [Tablet PC],SelBold property, IInkEdit.SelBold, IInkEdit.put_SelBold, IInkEdit::SelBold, IInkEdit::get_SelBold, IInkEdit::put_SelBold, InkEdit.get_SelBold, InkEdit.put_SelBold, NULL, SelBold property [Tablet PC], SelBold property [Tablet PC],IInkEdit interface, TRUE, get_SelBold, inked/IInkEdit::SelBold, inked/IInkEdit::get_SelBold, inked/IInkEdit::put_SelBold, put_SelBold, tablet.inkedit_selbold
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
 - IInkEdit::put_SelBold
 - inked/IInkEdit::put_SelBold
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
 - IInkEdit.SelBold
 - IInkEdit.get_SelBold
 - IInkEdit.put_SelBold
 - InkEdit.get_SelBold
 - InkEdit.put_SelBold
---

# IInkEdit::put_SelBold


## -description

Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is bold.

This property is read/write.

## -parameters

## -remarks

If a selection spans multiple characters with different bold styles, the <b>SelBold</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control, setting this property determines whether all new text entered at the current insertion point is bold.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
