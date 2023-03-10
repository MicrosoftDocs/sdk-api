---
UID: NF:msinkaut.IInkRecognitionAlternate.GetStrokesFromTextRange
title: IInkRecognitionAlternate::GetStrokesFromTextRange (msinkaut.h)
description: Retrieves the collection that corresponds to the smallest set of recognition segments that contains a specified character range within the alternate.
helpviewer_keywords: ["7dd8fa24-191f-465d-abd2-9a489df0324a","GetStrokesFromTextRange","GetStrokesFromTextRange method [Tablet PC]","GetStrokesFromTextRange method [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","GetStrokesFromTextRange method","IInkRecognitionAlternate.GetStrokesFromTextRange","IInkRecognitionAlternate::GetStrokesFromTextRange","msinkaut/IInkRecognitionAlternate::GetStrokesFromTextRange","tablet.iinkrecognitionalternate_getstrokesfromtextrange"]
old-location: tablet\iinkrecognitionalternate_getstrokesfromtextrange.htm
tech.root: tablet
ms.assetid: 7dd8fa24-191f-465d-abd2-9a489df0324a
ms.date: 12/05/2018
ms.keywords: 7dd8fa24-191f-465d-abd2-9a489df0324a, GetStrokesFromTextRange, GetStrokesFromTextRange method [Tablet PC], GetStrokesFromTextRange method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],GetStrokesFromTextRange method, IInkRecognitionAlternate.GetStrokesFromTextRange, IInkRecognitionAlternate::GetStrokesFromTextRange, msinkaut/IInkRecognitionAlternate::GetStrokesFromTextRange, tablet.iinkrecognitionalternate_getstrokesfromtextrange
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
 - IInkRecognitionAlternate::GetStrokesFromTextRange
 - msinkaut/IInkRecognitionAlternate::GetStrokesFromTextRange
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
 - IInkRecognitionAlternate.GetStrokesFromTextRange
---

# IInkRecognitionAlternate::GetStrokesFromTextRange


## -description

Retrieves the collection that corresponds to the smallest set of recognition segments that contains a specified character range within the alternate.

## -parameters

### -param selectionStart [in, out]

The start of the character range within this alternate. The character at the <i>selectionStart</i> position is included in the range of recognized text. This parameter is adjusted to the beginning of the smallest recognized set of one or more segments that includes the input selection. The <i>selectionStart</i> parameter is a zero-based index into the characters in the recognition alternate's text.

### -param selectionLength [in, out]

The length of the character range within the alternate. This parameter must be greater than 0. This parameter is adjusted to the length of the smallest set of one or more segments that includes the input selection.

### -param GetStrokesFromTextRange [out, retval]

Upon return, contains  a pointer to the collection of strokes that corresponds to the known range of recognized text.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate stroke handler helper object.

</td>
</tr>
</table>

## -remarks

To further clarify <b>GetStrokesFromTextRange</b>, consider a collection of strokes that has been recognized and for which the best alternate for those strokes is "how are you". The parameter passed to the method is some range within (or possibly all of) this string result. This alternate contains five segments, one for each word and one for each space. The strokes returned correspond to the smallest set of segments that include all of the input range. If the <i>selectionStart</i> parameter is 0, and the <i>selectionLength</i> parameter is 5, creating a range corresponding to the "how a" of the result string, then the strokes returned are all of the recognized strokes that make up the segments "how are". This is the smallest set of segments that includes the input range.

In both word and character based recognizers, spaces are counted as a character. If the input selection corresponds to a space character, then this method returns and empty <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromstrokeranges">GetStrokesFromStrokeRanges Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-gettextrangefromstrokes">GetTextRangeFromStrokes Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>