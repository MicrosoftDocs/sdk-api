---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Midline
title: IInkRecognitionAlternate::get_Midline (msinkaut.h)
description: Gets the midline for a IInkRecognitionAlternate object that represents a single line of text.
helpviewer_keywords: ["IInkRecognitionAlternate interface [Tablet PC]","Midline property","IInkRecognitionAlternate.Midline","IInkRecognitionAlternate.get_Midline","IInkRecognitionAlternate::Midline","IInkRecognitionAlternate::get_Midline","Midline property [Tablet PC]","Midline property [Tablet PC]","IInkRecognitionAlternate interface","ff12de3d-f760-4227-9406-634b19e66b4c","get_Midline","msinkaut/IInkRecognitionAlternate::Midline","msinkaut/IInkRecognitionAlternate::get_Midline","tablet.iinkrecognitionalternate_midline"]
old-location: tablet\iinkrecognitionalternate_midline.htm
tech.root: tablet
ms.assetid: ff12de3d-f760-4227-9406-634b19e66b4c
ms.date: 12/05/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],Midline property, IInkRecognitionAlternate.Midline, IInkRecognitionAlternate.get_Midline, IInkRecognitionAlternate::Midline, IInkRecognitionAlternate::get_Midline, Midline property [Tablet PC], Midline property [Tablet PC],IInkRecognitionAlternate interface, ff12de3d-f760-4227-9406-634b19e66b4c, get_Midline, msinkaut/IInkRecognitionAlternate::Midline, msinkaut/IInkRecognitionAlternate::get_Midline, tablet.iinkrecognitionalternate_midline
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
 - IInkRecognitionAlternate::get_Midline
 - msinkaut/IInkRecognitionAlternate::get_Midline
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
 - IInkRecognitionAlternate.Midline
 - IInkRecognitionAlternate.get_Midline
 - IInkRecognitionAlternate.get_Midline
---

# IInkRecognitionAlternate::get_Midline


## -description

Gets the midline for a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object that represents a single line of text.



This property is read-only.

## -parameters

## -remarks

The midline corresponds to an imaginary horizontal line with which the top of the main body of each character, excluding <i>ascender</i>, is aligned. The midline also corresponds to the top of the x-height.

<div class="alert"><b>Note</b>  <p class="note">If the recognition alternate  spans more than one recognition segment within a line of text, then this property returns a line parallel to the baseline for the alternate. The distance of the midline above the baseline is determined by the corresponding distance within the first segment.

<p class="note">You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="/windows/desktop/tablet/recognitionproperty-constants">Segmentation</a> recognition property globally unique identifier (GUID) to get a collection of one segment recognition alternates that correspond to a segmentation of your original alternate.

</div>
<div> </div>
<div class="alert"><b>Note</b>  If the recognition alternate spans more than one line, this property generates an E_FAIL error. You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property to get a collection of one line recognition alternates that corresponds to a multiple line recognition alternate.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_ascender">Ascender Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_baseline">Baseline Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_descender">Descender Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>