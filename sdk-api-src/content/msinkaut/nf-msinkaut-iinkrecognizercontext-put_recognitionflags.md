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

# IInkRecognizerContext::put_RecognitionFlags


## -description



Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.



This property is read/write.


## -parameters


## -remarks



The <b>RecognitionFlags</b> property gets or sets flags that specify things such as whether the recognizer treats all ink as a single word or whether the recognizer coerces the result based on the factoid that you specified for the context.

Setting the <b>RecognitionFlags</b> property succeeds only if the <a href="https://msdn.microsoft.com/af31559b-741e-4af2-8c35-9e34ad1af85f">Strokes</a> property is <b>NULL</b>.

For a list of modes that you can use, see the <a href="https://msdn.microsoft.com/ab9f4164-ea07-41d1-be6a-50009fa9464d">InkRecognitionModes</a> enumeration type.

<div class="alert"><b>Note</b>  You can combine modes using the bitwise <b>OR</b> operator.</div>
<div> </div>



## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/ab9f4164-ea07-41d1-be6a-50009fa9464d">InkRecognitionModes Enumeration</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

