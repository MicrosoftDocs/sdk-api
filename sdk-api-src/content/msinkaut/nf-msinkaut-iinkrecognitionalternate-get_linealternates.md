---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

