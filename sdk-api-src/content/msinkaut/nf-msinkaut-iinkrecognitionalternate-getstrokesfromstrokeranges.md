---
UID: NF:msinkaut.IInkRecognitionAlternate.GetStrokesFromStrokeRanges
title: IInkRecognitionAlternate::GetStrokesFromStrokeRanges (msinkaut.h)
description: Retrieves the smallest InkStrokes collection that contains a known input InkStrokes collection and for which the IInkRecognizer object can provide alternates.
helpviewer_keywords: ["25079651-4fcd-4f13-b73f-7d5ffefa871e","GetStrokesFromStrokeRanges","GetStrokesFromStrokeRanges method [Tablet PC]","GetStrokesFromStrokeRanges method [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","GetStrokesFromStrokeRanges method","IInkRecognitionAlternate.GetStrokesFromStrokeRanges","IInkRecognitionAlternate::GetStrokesFromStrokeRanges","msinkaut/IInkRecognitionAlternate::GetStrokesFromStrokeRanges","tablet.iinkrecognitionalternate_getstrokesfromstrokeranges"]
old-location: tablet\iinkrecognitionalternate_getstrokesfromstrokeranges.htm
tech.root: tablet
ms.assetid: 25079651-4fcd-4f13-b73f-7d5ffefa871e
ms.date: 12/05/2018
ms.keywords: 25079651-4fcd-4f13-b73f-7d5ffefa871e, GetStrokesFromStrokeRanges, GetStrokesFromStrokeRanges method [Tablet PC], GetStrokesFromStrokeRanges method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],GetStrokesFromStrokeRanges method, IInkRecognitionAlternate.GetStrokesFromStrokeRanges, IInkRecognitionAlternate::GetStrokesFromStrokeRanges, msinkaut/IInkRecognitionAlternate::GetStrokesFromStrokeRanges, tablet.iinkrecognitionalternate_getstrokesfromstrokeranges
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
 - IInkRecognitionAlternate::GetStrokesFromStrokeRanges
 - msinkaut/IInkRecognitionAlternate::GetStrokesFromStrokeRanges
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
 - IInkRecognitionAlternate.GetStrokesFromStrokeRanges
---

# IInkRecognitionAlternate::GetStrokesFromStrokeRanges


## -description

Retrieves the smallest <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that contains a known input InkStrokes collection and for which the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object can provide alternates.

## -parameters

### -param Strokes [in]

The collection of stroke objects to use to find the smallest stroke collection of the recognition result alternate that contains this collection.

### -param GetStrokesFromStrokeRanges [out, retval]

When this method returns, contains a pointer to the smallest collection of strokes that contains a known input collection of strokes and for which the recognizer can provide alternates.

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
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different Ink object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

The returned collection may match the input collection, or it may be larger if the input collection matches only part of the smallest recognition result that includes all of the input strokes.

This method is most useful for single-click word selection. For example, to return the strokes that make up the word you clicked, you can click a stroke, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-hittestcircle">HitTest</a> method of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object to retrieve the stroke that was clicked, and then call <b>GetStrokesFromStrokeRanges</b>.

The stroke ranges are valid until the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object is modified.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromtextrange">GetStrokesFromTextRange Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-gettextrangefromstrokes">GetTextRangeFromStrokes Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>