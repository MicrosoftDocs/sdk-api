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

# IInkRecognitionResult::get_TopConfidence


## -description



Gets the top alternate of the recognition result.



This property is read-only.


## -parameters


## -remarks



Of the Microsoft <b>recognizers</b>, only the Microsoft English (US) Handwriting Recognizer and the Microsoft Gesture Recognizer support confidence levels. Third party recognizers may or may not support confidence levels.

<div class="alert"><b>Note</b>  The <b>TopConfidence</b> property may change if a call to the <a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate</a> method causes a change to the <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> property.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d">InkRecognitionConfidence Enumeration</a>



<a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate Method</a>



<a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate Property</a>
 

 

