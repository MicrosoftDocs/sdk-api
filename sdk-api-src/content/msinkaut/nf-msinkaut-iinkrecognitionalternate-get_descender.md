---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Descender
title: IInkRecognitionAlternate::get_Descender (msinkaut.h)
author: windows-sdk-content
description: Gets the decender line for an IInkRecognitionAlternate object that represents a single line of text.
old-location: tablet\iinkrecognitionalternate_descender.htm
tech.root: tablet
ms.assetid: 52507911-b48c-47a9-8046-3000ed61e3c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 52507911-b48c-47a9-8046-3000ed61e3c8, Descender property [Tablet PC], Descender property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],Descender property, IInkRecognitionAlternate.Descender, IInkRecognitionAlternate.get_Descender, IInkRecognitionAlternate::Descender, IInkRecognitionAlternate::get_Descender, get_Descender, msinkaut/IInkRecognitionAlternate::Descender, msinkaut/IInkRecognitionAlternate::get_Descender, tablet.iinkrecognitionalternate_descender
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkRecognitionAlternate.Descender"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionAlternate.Descender
 - IInkRecognitionAlternate.get_Descender
 - IInkRecognitionAlternate.get_Descender
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionAlternate::get_Descender


## -description



Gets the decender line for an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object that represents a single line of text.



This property is read-only.


## -parameters


## -remarks



For western languages, the descender corresponds to the portion of a lowercase letter that falls below the baseline, such as the vertical line of a "p" that extends below the lowest point of the circle in that letter. The descender line is the imaginary horizontal line across the bottom of the descenders.

<div class="alert"><b>Note</b>  <p class="note">If the recognition alternate spans more than one recognition segment within a line of text, then this property returns a line parallel to the baseline for the alternate. The distance of the descender line below the baseline is determined by the corresponding distance within the first segment.

<p class="note">You can use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="https://docs.microsoft.com/windows/desktop/tablet/recognitionproperty-constants">Segmentation</a> recognition property globally unique identifier (GUID) to get a collection of one segment recognition alternates that correspond to a segmentation of your original alternate.

</div>
<div> </div>
<div class="alert"><b>Note</b>  If the recognition alternate spans more than one line, this property generates an E_FAIL error. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property to get a collection of one line recognition alternates that corresponds to a multiple line recognition alternate.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_ascender">Ascender Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_baseline">Baseline Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_midline">Midline Property [IInkRecognitionAlternate Interface]</a>
 

 

