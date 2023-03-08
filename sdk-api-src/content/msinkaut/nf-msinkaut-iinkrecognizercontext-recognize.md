---
UID: NF:msinkaut.IInkRecognizerContext.Recognize
title: IInkRecognizerContext::Recognize (msinkaut.h)
description: Performs recognition on an InkStrokes collection and returns recognition results. (IInkRecognizerContext.Recognize)
helpviewer_keywords: ["83695dfd-3634-47e7-8311-7216876a827a","IInkRecognizerContext interface [Tablet PC]","Recognize method","IInkRecognizerContext.Recognize","IInkRecognizerContext::Recognize","Recognize","Recognize method [Tablet PC]","Recognize method [Tablet PC]","IInkRecognizerContext interface","msinkaut/IInkRecognizerContext::Recognize","tablet.inkrecognizercontext_recognize"]
old-location: tablet\inkrecognizercontext_recognize.htm
tech.root: tablet
ms.assetid: 83695dfd-3634-47e7-8311-7216876a827a
ms.date: 12/05/2018
ms.keywords: 83695dfd-3634-47e7-8311-7216876a827a, IInkRecognizerContext interface [Tablet PC],Recognize method, IInkRecognizerContext.Recognize, IInkRecognizerContext::Recognize, Recognize, Recognize method [Tablet PC], Recognize method [Tablet PC],IInkRecognizerContext interface, msinkaut/IInkRecognizerContext::Recognize, tablet.inkrecognizercontext_recognize
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
 - IInkRecognizerContext::Recognize
 - msinkaut/IInkRecognizerContext::Recognize
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
 - IInkRecognizerContext.Recognize
---

# IInkRecognizerContext::Recognize


## -description

Performs recognition on an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and returns recognition results.

## -parameters

### -param RecognitionStatus [in, out]

The most recent <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus">InkRecognitionStatus</a> value.

### -param RecognitionResult [out, retval]

When this method returns, contains a pointer to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> results of a recognized collection of strokes, or else <b>NULL</b> if the recognizer could not compute a result for the ink.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>

## -remarks

This method performs recognition synchronously. To start background or asynchronous recognition, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize</a> or <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates">BackgroundRecognizeWithAlternates</a> methods.

You must use a try/catch block when calling <b>Recognize</b> because an exception is thrown when the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object contains no strokes or only deleted strokes.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates">BackgroundRecognizeWithAlternates Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
