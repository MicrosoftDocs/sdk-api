---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Baseline
title: IInkRecognitionAlternate::get_Baseline (msinkaut.h)
description: Gets the baseline for a IInkRecognitionAlternate object that represents a single line of text.
helpviewer_keywords: ["5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4","Baseline property [Tablet PC]","Baseline property [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","Baseline property","IInkRecognitionAlternate.Baseline","IInkRecognitionAlternate.get_Baseline","IInkRecognitionAlternate::Baseline","IInkRecognitionAlternate::get_Baseline","get_Baseline","msinkaut/IInkRecognitionAlternate::Baseline","msinkaut/IInkRecognitionAlternate::get_Baseline","tablet.iinkrecognitionalternate_baseline"]
old-location: tablet\iinkrecognitionalternate_baseline.htm
tech.root: tablet
ms.assetid: 5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4
ms.date: 12/05/2018
ms.keywords: 5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4, Baseline property [Tablet PC], Baseline property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],Baseline property, IInkRecognitionAlternate.Baseline, IInkRecognitionAlternate.get_Baseline, IInkRecognitionAlternate::Baseline, IInkRecognitionAlternate::get_Baseline, get_Baseline, msinkaut/IInkRecognitionAlternate::Baseline, msinkaut/IInkRecognitionAlternate::get_Baseline, tablet.iinkrecognitionalternate_baseline
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
 - IInkRecognitionAlternate::get_Baseline
 - msinkaut/IInkRecognitionAlternate::get_Baseline
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
 - IInkRecognitionAlternate.Baseline
 - IInkRecognitionAlternate.get_Baseline
 - IInkRecognitionAlternate.get_Baseline
---

# IInkRecognitionAlternate::get_Baseline


## -description

Gets the baseline for a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object that represents a single line of text.



This property is read-only.

## -parameters

## -remarks

The baseline is the imaginary horizontal line with which the base of each character, excluding decenders, is aligned. It also corresponds to the bottom of the x-height.

<div class="alert"><b>Note</b>  <p class="note">If the recognition alternate spans more than one recognition segment within a line of text, then this property returns a line that begins at the first point of the baseline of the first segment in the alternate and ends at the last point of the baseline of the last segment in the alternate.

<p class="note">You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="/windows/desktop/tablet/recognitionproperty-constants">Segmentation</a> recognition property globally unique identifier (GUID) to get a collection of one segment recognition alternates that correspond to a segmentation of your original alternate.

</div>
<div> </div>
<div class="alert"><b>Note</b>  If the recognition alternate spans more than one line, this property generates an E_FAIL error. You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property to get a collection of one line recognition alternates that corresponds to a multiple line recognition alternate.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_ascender">Ascender Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_descender">Descender Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_midline">Midline Property [IInkRecognitionAlternate Interface]</a>