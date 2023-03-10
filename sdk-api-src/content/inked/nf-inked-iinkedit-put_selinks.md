---
UID: NF:inked.IInkEdit.put_SelInks
title: IInkEdit::put_SelInks (inked.h)
description: Gets or sets the array of embedded InkDisp objects (if displayed as ink) in the current selection. (Put)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","SelInks property","IInkEdit.SelInks","IInkEdit.put_SelInks","IInkEdit::SelInks","IInkEdit::get_SelInks","IInkEdit::put_SelInks","InkEdit.get_SelInks","InkEdit.put_SelInks","SelInks property [Tablet PC]","SelInks property [Tablet PC]","IInkEdit interface","dbdd590d-a8d8-44e9-aecc-fbbe0d24ea20","get_SelInks","inked/IInkEdit::SelInks","inked/IInkEdit::get_SelInks","inked/IInkEdit::put_SelInks","put_SelInks","tablet.inkedit_selinks"]
old-location: tablet\inkedit_selinks.htm
tech.root: tablet
ms.assetid: dbdd590d-a8d8-44e9-aecc-fbbe0d24ea20
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],SelInks property, IInkEdit.SelInks, IInkEdit.put_SelInks, IInkEdit::SelInks, IInkEdit::get_SelInks, IInkEdit::put_SelInks, InkEdit.get_SelInks, InkEdit.put_SelInks, SelInks property [Tablet PC], SelInks property [Tablet PC],IInkEdit interface, dbdd590d-a8d8-44e9-aecc-fbbe0d24ea20, get_SelInks, inked/IInkEdit::SelInks, inked/IInkEdit::get_SelInks, inked/IInkEdit::put_SelInks, put_SelInks, tablet.inkedit_selinks
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
 - IInkEdit::put_SelInks
 - inked/IInkEdit::put_SelInks
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
 - IInkEdit.SelInks
 - IInkEdit.get_SelInks
 - IInkEdit.put_SelInks
 - InkEdit.get_SelInks
 - InkEdit.put_SelInks
---

# IInkEdit::put_SelInks


## -description

Gets or sets the array of embedded <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> objects (if displayed as ink) in the current selection.



This property is read/write.

## -parameters

## -remarks

Ink must be recognized before being accessed through this property. If it is not recognized first, the <b>SelInks</b> property always contains zero <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> objects. You must either call the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-recognize">Recognize</a> method (if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout">RecognitionTimeout</a> property equals 0) or wait until the ink is automatically recognized (when the value of the <b>RecognitionTimeout</b> property is greater than 0) to access ink through this property.

The <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control ignores any <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> on ink set through the <b>SelInks</b> property. Instead, the InkEdit control applies alternate drawing attributes according to the attributes of nearby text.

This property is run time only.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout">RecoTimeout Property</a>



<a href="/windows/desktop/api/inked/nf-inked-iinkedit-recognize">Recognize Method [InkEdit Control]</a>
