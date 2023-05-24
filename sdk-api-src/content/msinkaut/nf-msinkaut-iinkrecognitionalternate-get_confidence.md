---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Confidence
title: IInkRecognitionAlternate::get_Confidence (msinkaut.h)
description: Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture. (IInkRecognitionAlternate.get_Confidence)
helpviewer_keywords: ["049a5742-fc4f-4a9a-91d5-5eec56dc8e8b","Confidence property [Tablet PC]","Confidence property [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","Confidence property","IInkRecognitionAlternate.Confidence","IInkRecognitionAlternate.get_Confidence","IInkRecognitionAlternate::Confidence","IInkRecognitionAlternate::get_Confidence","get_Confidence","msinkaut/IInkRecognitionAlternate::Confidence","msinkaut/IInkRecognitionAlternate::get_Confidence","tablet.iinkrecognitionalternate_confidence"]
old-location: tablet\iinkrecognitionalternate_confidence.htm
tech.root: tablet
ms.assetid: 049a5742-fc4f-4a9a-91d5-5eec56dc8e8b
ms.date: 12/05/2018
ms.keywords: 049a5742-fc4f-4a9a-91d5-5eec56dc8e8b, Confidence property [Tablet PC], Confidence property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],Confidence property, IInkRecognitionAlternate.Confidence, IInkRecognitionAlternate.get_Confidence, IInkRecognitionAlternate::Confidence, IInkRecognitionAlternate::get_Confidence, get_Confidence, msinkaut/IInkRecognitionAlternate::Confidence, msinkaut/IInkRecognitionAlternate::get_Confidence, tablet.iinkrecognitionalternate_confidence
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
 - IInkRecognitionAlternate::get_Confidence
 - msinkaut/IInkRecognitionAlternate::get_Confidence
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
 - IInkRecognitionAlternate.Confidence
 - IInkRecognitionAlternate.get_Confidence
 - IInkRecognitionAlternate.get_Confidence
---

# IInkRecognitionAlternate::get_Confidence


## -description

Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object or a gesture.



This property is read-only.

## -parameters

## -remarks

For a list of confidence values that may be returned, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence">InkRecognitionConfidence</a> enumeration type.

<div class="alert"><b>Note</b>  Confidence evaluation is available for all gesture recognizers in the current release of Windows XP Tablet PC Edition.</div>
<div> </div>

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a> object:

If the alternate represents a phrase or sentence, the value represents the lowest confidence level of a recognition segment found in the phrase or sentence. However, if the alternate represents a word, the value represents the confidence level of the word.

<div class="alert"><b>Note</b>  This property throws an exception if the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a> that generates the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a> does not support confidence levels.</div>
<div> </div>
Of the Microsoft recognizers, only the Microsoft English (US) Handwriting Recognizer and the Microsoft Gesture Recognizer support confidence levels. Third party recognizers may or may not support confidence levels.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence">InkRecognitionConfidence Enumeration</a>
