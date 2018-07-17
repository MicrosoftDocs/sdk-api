---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Midline
title: IInkRecognitionAlternate::get_Midline
author: windows-sdk-content
description: Gets the midline for a IInkRecognitionAlternate object that represents a single line of text.
old-location: tablet\iinkrecognitionalternate_midline.htm
old-project: tablet
ms.assetid: ff12de3d-f760-4227-9406-634b19e66b4c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],Midline property, IInkRecognitionAlternate.Midline, IInkRecognitionAlternate.get_Midline, IInkRecognitionAlternate::Midline, IInkRecognitionAlternate::get_Midline, Midline property [Tablet PC], Midline property [Tablet PC],IInkRecognitionAlternate interface, ff12de3d-f760-4227-9406-634b19e66b4c, get_Midline, msinkaut/IInkRecognitionAlternate::Midline, msinkaut/IInkRecognitionAlternate::get_Midline, tablet.iinkrecognitionalternate_midline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionAlternate::get_Midline


## -description



Gets the midline for a <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object that represents a single line of text.



This property is read-only.


## -parameters


## -remarks



The midline corresponds to an imaginary horizontal line with which the top of the main body of each character, excluding <i>ascender</i>, is aligned. The midline also corresponds to the top of the x-height.

<div class="alert"><b>Note</b>  <p class="note">If the recognition alternate  spans more than one recognition segment within a line of text, then this property returns a line parallel to the baseline for the alternate. The distance of the midline above the baseline is determined by the corresponding distance within the first segment.

<p class="note">You can use the <a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">Segmentation</a> recognition property globally unique identifier (GUID) to get a collection of one segment recognition alternates that correspond to a segmentation of your original alternate.

</div>
<div> </div>
<div class="alert"><b>Note</b>  If the recognition alternate spans more than one line, this property generates an E_FAIL error. You can use the <a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates</a> property to get a collection of one line recognition alternates that corresponds to a multiple line recognition alternate.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues Method</a>



<a href="https://msdn.microsoft.com/4cc7bd86-e098-4de7-a73a-b878cba37e88">Ascender Property</a>



<a href="https://msdn.microsoft.com/5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4">Baseline Property</a>



<a href="https://msdn.microsoft.com/52507911-b48c-47a9-8046-3000ed61e3c8">Descender Property</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates Property</a>
 

 

