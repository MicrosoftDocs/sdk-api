---
UID: NF:msinkaut.IInkRecognizer2.get_UnicodeRanges
title: IInkRecognizer2::get_UnicodeRanges (msinkaut.h)
description: Retrieves the Unicode ranges set for the current recognizer.
helpviewer_keywords: ["IInkRecognizer2 interface [Tablet PC]","get_UnicodeRanges method","IInkRecognizer2.get_UnicodeRanges","IInkRecognizer2::get_UnicodeRanges","d53e68d3-4809-41ae-b709-d96986831039","get_UnicodeRanges","get_UnicodeRanges method [Tablet PC]","get_UnicodeRanges method [Tablet PC]","IInkRecognizer2 interface","msinkaut/IInkRecognizer2::get_UnicodeRanges","tablet.iinkrecognizer2_get_unicoderanges"]
old-location: tablet\iinkrecognizer2_get_unicoderanges.htm
tech.root: tablet
ms.assetid: d53e68d3-4809-41ae-b709-d96986831039
ms.date: 12/05/2018
ms.keywords: IInkRecognizer2 interface [Tablet PC],get_UnicodeRanges method, IInkRecognizer2.get_UnicodeRanges, IInkRecognizer2::get_UnicodeRanges, d53e68d3-4809-41ae-b709-d96986831039, get_UnicodeRanges, get_UnicodeRanges method [Tablet PC], get_UnicodeRanges method [Tablet PC],IInkRecognizer2 interface, msinkaut/IInkRecognizer2::get_UnicodeRanges, tablet.iinkrecognizer2_get_unicoderanges
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
 - IInkRecognizer2::get_UnicodeRanges
 - msinkaut/IInkRecognizer2::get_UnicodeRanges
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
 - IInkRecognizer2.get_UnicodeRanges
---

# IInkRecognizer2::get_UnicodeRanges


## -description

Retrieves the Unicode ranges set for the current recognizer.

## -parameters

### -param UnicodeRanges [out]

A VARIANT array containing the Unicode ranges being used by the recognizer. An array (VT_ARRAY) of long integers (VT_ARRAY|VT_UI4). The array consists of alternating pairs for each range. For each pair in the array, the first value specifies the low Unicode code point in the range of supported Unicode points, and the second value specifies the number of Unicode points in the range.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer2">IInkRecognizer2 Interface</a>