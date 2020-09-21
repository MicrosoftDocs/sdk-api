---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Ascender
title: IInkRecognitionAlternate::get_Ascender (msinkaut.h)
description: Gets the ascender line for a IInkRecognitionAlternate object that represents a single line of text.
helpviewer_keywords: ["4cc7bd86-e098-4de7-a73a-b878cba37e88","Ascender property [Tablet PC]","Ascender property [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","Ascender property","IInkRecognitionAlternate.Ascender","IInkRecognitionAlternate.get_Ascender","IInkRecognitionAlternate::Ascender","IInkRecognitionAlternate::get_Ascender","get_Ascender","msinkaut/IInkRecognitionAlternate::Ascender","msinkaut/IInkRecognitionAlternate::get_Ascender","tablet.iinkrecognitionalternate_ascender"]
old-location: tablet\iinkrecognitionalternate_ascender.htm
tech.root: tablet
ms.assetid: 4cc7bd86-e098-4de7-a73a-b878cba37e88
ms.date: 12/05/2018
ms.keywords: 4cc7bd86-e098-4de7-a73a-b878cba37e88, Ascender property [Tablet PC], Ascender property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],Ascender property, IInkRecognitionAlternate.Ascender, IInkRecognitionAlternate.get_Ascender, IInkRecognitionAlternate::Ascender, IInkRecognitionAlternate::get_Ascender, get_Ascender, msinkaut/IInkRecognitionAlternate::Ascender, msinkaut/IInkRecognitionAlternate::get_Ascender, tablet.iinkrecognitionalternate_ascender
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
 - IInkRecognitionAlternate::get_Ascender
 - msinkaut/IInkRecognitionAlternate::get_Ascender
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
 - IInkRecognitionAlternate.Ascender
 - IInkRecognitionAlternate.get_Ascender
 - IInkRecognitionAlternate.get_Ascender
---

# IInkRecognitionAlternate::get_Ascender


## -description

Gets the ascender line for a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object that represents a single line of text.



This property is read-only.

## -parameters

## -remarks

For western languages, the ascender corresponds to the portion of a lowercase letter that extends above the main body (the midline or x-height) of that letter such as the vertical line of a "b" that extends above the highest point of the circle in that letter. The ascender line is the imaginary horizontal line across the top of the ascenders.

<div class="alert"><b>Note</b>  If the recognition alternate spans more than one recognition segment within a line of text, then this property will return a line parallel to the baseline for the alternate. The distance of the ascender line above the baseline is determined by the corresponding distance within the first segment.You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="/windows/desktop/tablet/recognitionproperty-constants">Segmentation</a> recognition property globally unique identifier (GUID) to get a collection of one segment recognition alternates that correspond to a segmentation of your original alternate.</div>
<div> </div>
<div class="alert"><b>Note</b>  If the recognition alternate spans more than one line, this property generates an E_FAIL error. You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property to get a collection of one line recognition alternates that corresponds to a multiple line recognition alternate.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_baseline">Baseline Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_descender">Descender Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_midline">Midline Property [IInkRecognitionAlternate Interface]</a>