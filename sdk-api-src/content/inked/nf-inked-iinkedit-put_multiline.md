---
UID: NF:inked.IInkEdit.put_MultiLine
title: IInkEdit::put_MultiLine (inked.h)
description: Gets or sets a value indicating whether an InkEdit control can accept and display multiple lines of text. (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","MultiLine property","IInkEdit.MultiLine","IInkEdit.put_MultiLine","IInkEdit::MultiLine","IInkEdit::get_MultiLine","IInkEdit::put_MultiLine","InkEdit.get_MultiLine","InkEdit.put_MultiLine","MultiLine property [Tablet PC]","MultiLine property [Tablet PC]","IInkEdit interface","get_MultiLine","inked/IInkEdit::MultiLine","inked/IInkEdit::get_MultiLine","inked/IInkEdit::put_MultiLine","put_MultiLine","tablet.inkedit_multiline"]
old-location: tablet\inkedit_multiline.htm
tech.root: tablet
ms.assetid: 361cfaea-d961-423c-98b0-f04bd7e621e9
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],MultiLine property, IInkEdit.MultiLine, IInkEdit.put_MultiLine, IInkEdit::MultiLine, IInkEdit::get_MultiLine, IInkEdit::put_MultiLine, InkEdit.get_MultiLine, InkEdit.put_MultiLine, MultiLine property [Tablet PC], MultiLine property [Tablet PC],IInkEdit interface, get_MultiLine, inked/IInkEdit::MultiLine, inked/IInkEdit::get_MultiLine, inked/IInkEdit::put_MultiLine, put_MultiLine, tablet.inkedit_multiline
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
 - IInkEdit::put_MultiLine
 - inked/IInkEdit::put_MultiLine
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
 - IInkEdit.MultiLine
 - IInkEdit.get_MultiLine
 - IInkEdit.put_MultiLine
 - InkEdit.get_MultiLine
 - InkEdit.put_MultiLine
---

# IInkEdit::put_MultiLine


## -description

 Gets or sets a value indicating whether an <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control can accept and display multiple lines of text.


This property is read/write.

## -parameters

## -remarks

A multiple-line <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control wraps text as the user types text extending beyond the text box.



You can also add scroll bars to a larger <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control using the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars">ScrollBars</a> property. If no HScrollBar control (horizontal scroll bar) is specified, the text in a multiple-line InkEdit control automatically wraps.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
