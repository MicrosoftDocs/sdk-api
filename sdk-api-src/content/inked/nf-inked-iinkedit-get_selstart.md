---
UID: NF:inked.IInkEdit.get_SelStart
title: IInkEdit::get_SelStart (inked.h)
description: Gets or sets the starting point of the text that is selected in the InkEdit control (run time only). (Get)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelStart property","IInkEdit.SelStart","IInkEdit.get_SelStart","IInkEdit::SelStart","IInkEdit::get_SelStart","IInkEdit::put_SelStart","InkEdit.get_SelStart","InkEdit.put_SelStart","SelStart property [Tablet PC]","SelStart property [Tablet PC]","IInkEdit interface","get_SelStart","inked/IInkEdit::SelStart","inked/IInkEdit::get_SelStart","inked/IInkEdit::put_SelStart","put_SelStart","tablet.inkedit_selstart"]
old-location: tablet\inkedit_selstart.htm
tech.root: tablet
ms.assetid: 5f8925c0-ec62-425e-a020-9c534056e63f
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelStart property, IInkEdit.SelStart, IInkEdit.get_SelStart, IInkEdit::SelStart, IInkEdit::get_SelStart, IInkEdit::put_SelStart, InkEdit.get_SelStart, InkEdit.put_SelStart, SelStart property [Tablet PC], SelStart property [Tablet PC],IInkEdit interface, get_SelStart, inked/IInkEdit::SelStart, inked/IInkEdit::get_SelStart, inked/IInkEdit::put_SelStart, put_SelStart, tablet.inkedit_selstart
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
 - IInkEdit::get_SelStart
 - inked/IInkEdit::get_SelStart
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
 - IInkEdit.SelStart
 - IInkEdit.get_SelStart
 - IInkEdit.put_SelStart
 - InkEdit.get_SelStart
 - InkEdit.put_SelStart
---

# IInkEdit::get_SelStart


## -description

Gets or sets the starting point of the text that is selected in the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

This property is read/write.

## -parameters

## -remarks

Setting <b>SelStart</b> greater than the text length sets the property to the existing text length; changing <b>SelStart</b> changes the selection to an insertion point and sets <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength">SelLength</a> to 0.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
