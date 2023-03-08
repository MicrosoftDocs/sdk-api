---
UID: NF:inked.IInkEdit.get_RecognitionTimeout
title: IInkEdit::get_RecognitionTimeout (inked.h)
description: Gets or sets the length of time, in milliseconds, between the last IInkStrokeDisp object collected and the beginning of text recognition. (Get)
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","RecognitionTimeout property","IInkEdit.RecognitionTimeout","IInkEdit.get_RecognitionTimeout","IInkEdit::RecognitionTimeout","IInkEdit::get_RecognitionTimeout","IInkEdit::put_RecognitionTimeout","InkEdit.get_RecognitionTimeout","InkEdit.put_RecognitionTimeout","RecognitionTimeout property [Tablet PC]","RecognitionTimeout property [Tablet PC]","IInkEdit interface","e1171aa3-841f-433e-88b8-e3fc63129aeb","get_RecognitionTimeout","inked/IInkEdit::RecognitionTimeout","inked/IInkEdit::get_RecognitionTimeout","inked/IInkEdit::put_RecognitionTimeout","put_RecognitionTimeout","tablet.inkedit_recotimeout"]
old-location: tablet\inkedit_recotimeout.htm
tech.root: tablet
ms.assetid: e1171aa3-841f-433e-88b8-e3fc63129aeb
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],RecognitionTimeout property, IInkEdit.RecognitionTimeout, IInkEdit.get_RecognitionTimeout, IInkEdit::RecognitionTimeout, IInkEdit::get_RecognitionTimeout, IInkEdit::put_RecognitionTimeout, InkEdit.get_RecognitionTimeout, InkEdit.put_RecognitionTimeout, RecognitionTimeout property [Tablet PC], RecognitionTimeout property [Tablet PC],IInkEdit interface, e1171aa3-841f-433e-88b8-e3fc63129aeb, get_RecognitionTimeout, inked/IInkEdit::RecognitionTimeout, inked/IInkEdit::get_RecognitionTimeout, inked/IInkEdit::put_RecognitionTimeout, put_RecognitionTimeout, tablet.inkedit_recotimeout
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
 - IInkEdit::get_RecognitionTimeout
 - inked/IInkEdit::get_RecognitionTimeout
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
 - IInkEdit.RecognitionTimeout
 - IInkEdit.get_RecognitionTimeout
 - IInkEdit.put_RecognitionTimeout
 - InkEdit.get_RecognitionTimeout
 - InkEdit.put_RecognitionTimeout
---

# IInkEdit::get_RecognitionTimeout


## -description

Gets or sets the length of time, in milliseconds, between the last <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object collected and the beginning of text recognition.



This property is read/write.

## -parameters

## -remarks

Setting this property equal to zero prevents the ink from being replaced by the recognized text.

## -see-also

<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
