---
UID: NF:msinkaut.IInkRecognitionAlternate.GetTextRangeFromStrokes
title: IInkRecognitionAlternate::GetTextRangeFromStrokes (msinkaut.h)
description: Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known InkStrokes collection.
helpviewer_keywords: ["GetTextRangeFromStrokes","GetTextRangeFromStrokes method [Tablet PC]","GetTextRangeFromStrokes method [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","GetTextRangeFromStrokes method","IInkRecognitionAlternate.GetTextRangeFromStrokes","IInkRecognitionAlternate::GetTextRangeFromStrokes","b481e356-0a3c-4437-9700-6d8badcb0b0b","msinkaut/IInkRecognitionAlternate::GetTextRangeFromStrokes","tablet.iinkrecognitionalternate_gettextrangefromstrokes"]
old-location: tablet\iinkrecognitionalternate_gettextrangefromstrokes.htm
tech.root: tablet
ms.assetid: b481e356-0a3c-4437-9700-6d8badcb0b0b
ms.date: 12/05/2018
ms.keywords: GetTextRangeFromStrokes, GetTextRangeFromStrokes method [Tablet PC], GetTextRangeFromStrokes method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],GetTextRangeFromStrokes method, IInkRecognitionAlternate.GetTextRangeFromStrokes, IInkRecognitionAlternate::GetTextRangeFromStrokes, b481e356-0a3c-4437-9700-6d8badcb0b0b, msinkaut/IInkRecognitionAlternate::GetTextRangeFromStrokes, tablet.iinkrecognitionalternate_gettextrangefromstrokes
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
 - IInkRecognitionAlternate::GetTextRangeFromStrokes
 - msinkaut/IInkRecognitionAlternate::GetTextRangeFromStrokes
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
 - IInkRecognitionAlternate.GetTextRangeFromStrokes
---

# IInkRecognitionAlternate::GetTextRangeFromStrokes


## -description

Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.

## -parameters

### -param Strokes [in]

The collection of strokes for which to find the containing alternate.

### -param selectionStart [in, out]

The start position of the range of recognized text within the alternate object on which this method was called that matches the smallest alternate that contains the passed-in strokes.

### -param selectionLength [in, out]

When this method returns, contains the length of the text within the range of recognized text of the smallest alternate that contains the passed-in strokes.

## -returns

If successful, returns S_OK; otherwise, returns an HRESULT error code.

## -remarks

Use this method to retrieve the text that corresponds to a specified range of strokes. For example, consider a collection of strokes, "how are you", that was drawn using nine strokes (one for each letter and three for each word). If a collection that consists of the sixth and seventh strokes is passed in, corresponding to characters "e" and "y", the text range returned matches the alternate containing "are you" and the selection start and length matches this substring.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromstrokeranges">GetStrokesFromStrokeRanges Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getstrokesfromtextrange">GetStrokesFromTextRange Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>