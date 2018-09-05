---
UID: NF:msinkaut.IInkRecognitionAlternate.get_LineAlternates
title: IInkRecognitionAlternate::get_LineAlternates
author: windows-sdk-content
description: Gets the IInkRecognitionAlternates collection in which each alternate in the collection is on a separate line.
old-location: tablet\iinkrecognitionalternate_linealternates.htm
old-project: tablet
ms.assetid: ccdf3092-b0a0-4626-b614-164548b1ca72
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],LineAlternates property, IInkRecognitionAlternate.LineAlternates, IInkRecognitionAlternate.get_LineAlternates, IInkRecognitionAlternate::LineAlternates, IInkRecognitionAlternate::get_LineAlternates, LineAlternates property [Tablet PC], LineAlternates property [Tablet PC],IInkRecognitionAlternate interface, ccdf3092-b0a0-4626-b614-164548b1ca72, get_LineAlternates, msinkaut/IInkRecognitionAlternate::LineAlternates, msinkaut/IInkRecognitionAlternate::get_LineAlternates, tablet.iinkrecognitionalternate_linealternates
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
 - IInkRecognitionAlternate.LineAlternates
 - IInkRecognitionAlternate.get_LineAlternates
 - IInkRecognitionAlternate.get_LineAlternates
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionAlternate::get_LineAlternates


## -description



Gets the <a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates</a> collection in which each alternate in the collection is on a separate line.



This property is read-only.


## -parameters


## -remarks



If you have a recognition alternate for a paragraph of ink, you can use the <b>LineAlternates</b> property to get a collection of recognition alternates in which each alternate represents a separate line of the paragraph.

This property is an alternative to calling the <a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">LineNumber</a> value of the RecognitionProperty constants. For more information about properties of alternates see the RecognitionProperty constants.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object automatically determines the line metrics when drawing ink.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues Method</a>



<a href="https://msdn.microsoft.com/ef3ab614-7aff-4660-bb2a-783f14e75b94">ConfidenceAlternates Property</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates Interface</a>



<a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty Constants</a>
 

 

