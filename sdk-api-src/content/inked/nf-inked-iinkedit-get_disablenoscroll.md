---
UID: NF:inked.IInkEdit.get_DisableNoScroll
title: IInkEdit::get_DisableNoScroll (inked.h)
description: Gets or sets a value that determines whether scroll bars in the InkEdit control are disabled. (Get)
helpviewer_keywords: ["DisableNoScroll property [Tablet PC]","DisableNoScroll property [Tablet PC]","IInkEdit interface","IInkEdit interface [Tablet PC]","DisableNoScroll property","IInkEdit.DisableNoScroll","IInkEdit.get_DisableNoScroll","IInkEdit::DisableNoScroll","IInkEdit::get_DisableNoScroll","IInkEdit::put_DisableNoScroll","InkEdit.get_DisableNoScroll","InkEdit.put_DisableNoScroll","get_DisableNoScroll","inked/IInkEdit::DisableNoScroll","inked/IInkEdit::get_DisableNoScroll","inked/IInkEdit::put_DisableNoScroll","put_DisableNoScroll","tablet.inkedit_disablenoscroll"]
old-location: tablet\inkedit_disablenoscroll.htm
tech.root: tablet
ms.assetid: 44a8372c-6323-4d76-9038-d61d210990b0
ms.date: 12/05/2018
ms.keywords: DisableNoScroll property [Tablet PC], DisableNoScroll property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],DisableNoScroll property, IInkEdit.DisableNoScroll, IInkEdit.get_DisableNoScroll, IInkEdit::DisableNoScroll, IInkEdit::get_DisableNoScroll, IInkEdit::put_DisableNoScroll, InkEdit.get_DisableNoScroll, InkEdit.put_DisableNoScroll, get_DisableNoScroll, inked/IInkEdit::DisableNoScroll, inked/IInkEdit::get_DisableNoScroll, inked/IInkEdit::put_DisableNoScroll, put_DisableNoScroll, tablet.inkedit_disablenoscroll
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
 - IInkEdit::get_DisableNoScroll
 - inked/IInkEdit::get_DisableNoScroll
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
 - IInkEdit.DisableNoScroll
 - IInkEdit.get_DisableNoScroll
 - IInkEdit.put_DisableNoScroll
 - InkEdit.get_DisableNoScroll
 - InkEdit.put_DisableNoScroll
---

# IInkEdit::get_DisableNoScroll


## -description

Gets or sets a value that determines whether scroll bars in the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control are disabled.

This property is read/write.

## -parameters

## -remarks

The <b>DisableNoScroll</b> property is ignored when the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars">ScrollBars</a> property is set to <b>rtfNone</b>. However, when <b>ScrollBars</b> is set to <b>rtfHorizontal</b>, <b>rtfVertical</b>, or <b>rtfBoth</b>, individual scroll bars are disabled when there are too few lines of text to scroll vertically or too few characters of text to scroll horizontally in the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.



This property is read-only at run time.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
