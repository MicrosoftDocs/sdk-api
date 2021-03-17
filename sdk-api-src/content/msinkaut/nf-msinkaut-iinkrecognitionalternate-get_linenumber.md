---
UID: NF:msinkaut.IInkRecognitionAlternate.get_LineNumber
title: IInkRecognitionAlternate::get_LineNumber (msinkaut.h)
description: Gets the line number of the ink that makes up the alternate.
helpviewer_keywords: ["IInkRecognitionAlternate interface [Tablet PC]","LineNumber property","IInkRecognitionAlternate.LineNumber","IInkRecognitionAlternate.get_LineNumber","IInkRecognitionAlternate::LineNumber","IInkRecognitionAlternate::get_LineNumber","LineNumber property [Tablet PC]","LineNumber property [Tablet PC]","IInkRecognitionAlternate interface","dd5578e7-7361-4e42-a503-2914f90a801f","get_LineNumber","msinkaut/IInkRecognitionAlternate::LineNumber","msinkaut/IInkRecognitionAlternate::get_LineNumber","tablet.iinkrecognitionalternate_linenumber"]
old-location: tablet\iinkrecognitionalternate_linenumber.htm
tech.root: tablet
ms.assetid: dd5578e7-7361-4e42-a503-2914f90a801f
ms.date: 12/05/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],LineNumber property, IInkRecognitionAlternate.LineNumber, IInkRecognitionAlternate.get_LineNumber, IInkRecognitionAlternate::LineNumber, IInkRecognitionAlternate::get_LineNumber, LineNumber property [Tablet PC], LineNumber property [Tablet PC],IInkRecognitionAlternate interface, dd5578e7-7361-4e42-a503-2914f90a801f, get_LineNumber, msinkaut/IInkRecognitionAlternate::LineNumber, msinkaut/IInkRecognitionAlternate::get_LineNumber, tablet.iinkrecognitionalternate_linenumber
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognitionAlternate::get_LineNumber
 - msinkaut/IInkRecognitionAlternate::get_LineNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionAlternate.LineNumber
 - IInkRecognitionAlternate.get_LineNumber
 - IInkRecognitionAlternate.get_LineNumber
---

# IInkRecognitionAlternate::get_LineNumber


## -description

Gets the line number of the ink that makes up the alternate.



This property is read-only.

## -parameters

## -remarks

Line numbers begin with 1.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">Recognizer</a> object automatically determines the metrics for how lines are spaced.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>