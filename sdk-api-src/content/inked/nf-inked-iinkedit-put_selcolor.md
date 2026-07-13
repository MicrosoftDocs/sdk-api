---
UID: NF:inked.IInkEdit.put_SelColor
title: IInkEdit::put_SelColor (inked.h)
description: Gets or sets the text color of the current text selection or insertion point (run time only). (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelColor property","IInkEdit.SelColor","IInkEdit.put_SelColor","IInkEdit::SelColor","IInkEdit::get_SelColor","IInkEdit::put_SelColor","InkEdit.get_SelColor","InkEdit.put_SelColor","SelColor property [Tablet PC]","SelColor property [Tablet PC]","IInkEdit interface","get_SelColor","inked/IInkEdit::SelColor","inked/IInkEdit::get_SelColor","inked/IInkEdit::put_SelColor","put_SelColor","tablet.inkedit_selcolor"]
old-location: tablet\inkedit_selcolor.htm
tech.root: tablet
ms.assetid: 06a4ed72-e2c2-4422-8796-39a65b19415e
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelColor property, IInkEdit.SelColor, IInkEdit.put_SelColor, IInkEdit::SelColor, IInkEdit::get_SelColor, IInkEdit::put_SelColor, InkEdit.get_SelColor, InkEdit.put_SelColor, SelColor property [Tablet PC], SelColor property [Tablet PC],IInkEdit interface, get_SelColor, inked/IInkEdit::SelColor, inked/IInkEdit::get_SelColor, inked/IInkEdit::put_SelColor, put_SelColor, tablet.inkedit_selcolor
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkEdit::put_SelColor
 - inked/IInkEdit::put_SelColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inked.h
api_name:
 - IInkEdit.SelColor
 - IInkEdit.get_SelColor
 - IInkEdit.put_SelColor
 - InkEdit.get_SelColor
 - InkEdit.put_SelColor
---

# IInkEdit::put_SelColor


## -description

Gets or sets the text color of the current text selection or insertion point (run time only).

This property is read/write.

## -parameters

## -remarks

If a selection spans multiple characters with different colors, the <b>SelColor</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control, setting this property determines the color of all new text entered at the current insertion point.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
