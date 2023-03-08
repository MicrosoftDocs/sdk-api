---
UID: NF:inked.IInkEdit.put_SelItalic
title: IInkEdit::put_SelItalic (inked.h)
description: Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is italic (run time only). (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelItalic property","IInkEdit.SelItalic","IInkEdit.put_SelItalic","IInkEdit::SelItalic","IInkEdit::get_SelItalic","IInkEdit::put_SelItalic","InkEdit.get_SelItalic","InkEdit.put_SelItalic","SelItalic property [Tablet PC]","SelItalic property [Tablet PC]","IInkEdit interface","get_SelItalic","inked/IInkEdit::SelItalic","inked/IInkEdit::get_SelItalic","inked/IInkEdit::put_SelItalic","put_SelItalic","tablet.inkedit_selitalic"]
old-location: tablet\inkedit_selitalic.htm
tech.root: tablet
ms.assetid: ea6f6495-d740-4aad-8310-7ce43f36cd93
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelItalic property, IInkEdit.SelItalic, IInkEdit.put_SelItalic, IInkEdit::SelItalic, IInkEdit::get_SelItalic, IInkEdit::put_SelItalic, InkEdit.get_SelItalic, InkEdit.put_SelItalic, SelItalic property [Tablet PC], SelItalic property [Tablet PC],IInkEdit interface, get_SelItalic, inked/IInkEdit::SelItalic, inked/IInkEdit::get_SelItalic, inked/IInkEdit::put_SelItalic, put_SelItalic, tablet.inkedit_selitalic
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
 - IInkEdit::put_SelItalic
 - inked/IInkEdit::put_SelItalic
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
 - IInkEdit.SelItalic
 - IInkEdit.get_SelItalic
 - IInkEdit.put_SelItalic
 - InkEdit.get_SelItalic
 - InkEdit.put_SelItalic
---

# IInkEdit::put_SelItalic


## -description

Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control is italic (run time only).

This property is read/write.

## -parameters

## -remarks

If a selection spans multiple italicized and un-italicized characters, the <b>SelItalic</b> property will be <b>NULL</b>.

If there is no text selected in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control, setting this property indicates all new text entered at the current insertion point will be italicized.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
