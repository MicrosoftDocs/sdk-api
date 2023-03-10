---
UID: NF:msinkaut.IInkRecognizerContext.BackgroundRecognizeWithAlternates
title: IInkRecognizerContext::BackgroundRecognizeWithAlternates (msinkaut.h)
description: Causes the IInkRecognizer object to recognize the associated strokes collection and fire a RecognitionWithAlternates event when recognition is complete.
helpviewer_keywords: ["1559678c-c220-4c67-aa0f-566377d95818","BackgroundRecognizeWithAlternates","BackgroundRecognizeWithAlternates method [Tablet PC]","BackgroundRecognizeWithAlternates method [Tablet PC]","IInkRecognizerContext interface","IInkRecognizerContext","IInkRecognizerContext interface [Tablet PC]","BackgroundRecognizeWithAlternates method","IInkRecognizerContext.BackgroundRecognizeWithAlternates","IInkRecognizerContext::BackgroundRecognizeWithAlternates","msinkaut/IInkRecognizerContext::BackgroundRecognizeWithAlternates","tablet.inkrecognizercontext_backgroundrecognizewithalternates"]
old-location: tablet\inkrecognizercontext_backgroundrecognizewithalternates.htm
tech.root: tablet
ms.assetid: 1559678c-c220-4c67-aa0f-566377d95818
ms.date: 12/05/2018
ms.keywords: 1559678c-c220-4c67-aa0f-566377d95818, BackgroundRecognizeWithAlternates, BackgroundRecognizeWithAlternates method [Tablet PC], BackgroundRecognizeWithAlternates method [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext, IInkRecognizerContext interface [Tablet PC],BackgroundRecognizeWithAlternates method, IInkRecognizerContext.BackgroundRecognizeWithAlternates, IInkRecognizerContext::BackgroundRecognizeWithAlternates, msinkaut/IInkRecognizerContext::BackgroundRecognizeWithAlternates, tablet.inkrecognizercontext_backgroundrecognizewithalternates
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
 - IInkRecognizerContext::BackgroundRecognizeWithAlternates
 - msinkaut/IInkRecognizerContext::BackgroundRecognizeWithAlternates
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
 - IInkRecognizerContext.BackgroundRecognizeWithAlternates
---

# IInkRecognizerContext::BackgroundRecognizeWithAlternates


## -description

Causes the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="/windows/desktop/tablet/inkrecognizercontext-recognitionwithalternates">RecognitionWithAlternates</a> event when recognition is complete.

## -parameters

### -param CustomData [in, optional]

Optional. Specifies any application-defined data that is available to the application in the <a href="/windows/desktop/tablet/inkrecognizercontext-recognitionwithalternates">RecognitionWithAlternates</a> event. This parameter may be a VARIANT of type VT_EMPTY or VT_NULL if no data needs to be passed. The default value is <b>NULL</b>.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>HRESULT Value</th>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_NO_STROKES_TO_RECOGNIZE</b></dt>
</dl>
</td>
<td width="60%">
No strokes exist.

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
</table>

## -remarks

This method specifies that ink recognition is performed asynchronously.

To perform recognition that includes only the best result string with no alternates, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize</a> method.

The <a href="/windows/desktop/tablet/inkrecognizercontext-recognitionwithalternates">RecognitionWithAlternates</a> event is not raised if the recognizer does not recognize any alternates.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize">BackgroundRecognize Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkextendedproperty-get_data">Data Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
