---
UID: NF:inked.IInkEdit.get_SelText
title: IInkEdit::get_SelText (inked.h)
description: Gets or sets the selected text within the InkEdit control (run time only). (Get)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelText property","IInkEdit.SelText","IInkEdit.get_SelText","IInkEdit::SelText","IInkEdit::get_SelText","IInkEdit::put_SelText","InkEdit.get_SelText","InkEdit.put_SelText","SelText property [Tablet PC]","SelText property [Tablet PC]","IInkEdit interface","get_SelText","inked/IInkEdit::SelText","inked/IInkEdit::get_SelText","inked/IInkEdit::put_SelText","put_SelText","tablet.inkedit_seltext"]
old-location: tablet\inkedit_seltext.htm
tech.root: tablet
ms.assetid: 2cd805b5-f421-48d1-9678-b3cae0bc6b86
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelText property, IInkEdit.SelText, IInkEdit.get_SelText, IInkEdit::SelText, IInkEdit::get_SelText, IInkEdit::put_SelText, InkEdit.get_SelText, InkEdit.put_SelText, SelText property [Tablet PC], SelText property [Tablet PC],IInkEdit interface, get_SelText, inked/IInkEdit::SelText, inked/IInkEdit::get_SelText, inked/IInkEdit::put_SelText, put_SelText, tablet.inkedit_seltext
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
 - IInkEdit::get_SelText
 - inked/IInkEdit::get_SelText
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
 - IInkEdit.SelText
 - IInkEdit.get_SelText
 - IInkEdit.put_SelText
 - InkEdit.get_SelText
 - InkEdit.put_SelText
---

# IInkEdit::get_SelText


## -description

Gets or sets the selected text within the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

This property is read/write.

## -parameters

## -remarks

Setting <b>SelText</b> to a new value sets <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength">SelLength</a> to 0 and replaces the selected text with the new string.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
