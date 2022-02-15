---
UID: NN:msinkaut.IInkRecognitionResult
title: IInkRecognitionResult (msinkaut.h)
description: Represents the result of the recognition. The results of recognizing handwritten ink are returned in an IInkRecognitionResult object.
helpviewer_keywords: ["IInkRecognitionResult","IInkRecognitionResult interface [Tablet PC]","IInkRecognitionResult interface [Tablet PC]","described","fd7ee250-6f76-419b-8164-0d2717ea288c","msinkaut/IInkRecognitionResult","tablet.iinkrecognitionresult"]
old-location: tablet\iinkrecognitionresult.htm
tech.root: tablet
ms.assetid: fd7ee250-6f76-419b-8164-0d2717ea288c
ms.date: 12/05/2018
ms.keywords: IInkRecognitionResult, IInkRecognitionResult interface [Tablet PC], IInkRecognitionResult interface [Tablet PC],described, fd7ee250-6f76-419b-8164-0d2717ea288c, msinkaut/IInkRecognitionResult, tablet.iinkrecognitionresult
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
 - IInkRecognitionResult
 - msinkaut/IInkRecognitionResult
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
 - IInkRecognitionResult
---

# IInkRecognitionResult interface


## -description

Represents the result of the recognition. The results of recognizing handwritten ink are returned in an <b>IInkRecognitionResult</b> object.

## -inheritance

The <b>IInkRecognitionResult</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognitionResult</b> also has these types of members:

## -remarks

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> objects, or alternates, are created from the result. The best, or top, alternate is the one that is used by the default in the result. However, you can use the methods of the <b>IInkRecognitionResult</b> object to specify which alternates to use in the result.

System performance can suffer if recognition results are automatically assigned to every collection of stroke. Therefore, by default, results are not attached to a collection of strokes. You must call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-setresultonstrokes">SetResultOnStrokes</a> method to assign results to a collection of strokes.

The only way to persist recognition results is to call <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-setresultonstrokes">SetResultOnStrokes</a> and then add this collection of strokes to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">CustomStrokes</a> collection on the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

Not all recognizers set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topconfidence">TopConfidence</a> property. When an application attempts to access a property that is not set by the recognizer, an argument exception is thrown.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

<div class="alert"><b>Note</b>  The various handwriting recognizers shipped from Microsoft in both Latin characters  and East Asian languages can sometimes produce the Unicode value 0xFFFF as the recognition result. This occurs when the recognizer is unable to match a piece of ink with any valid character. The 0xFFFF code point is valid UCS-2, but not allowed in UTF-8. An application that converts recognition results to UTF-8, should replace 0xFFFF with some other code point, for example, 0xFFFD.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes">CustomStrokes Property [InkDisp Class]</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
