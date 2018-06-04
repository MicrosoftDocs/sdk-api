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

# IHandwrittenTextInsertion::InsertInkRecognitionResult


## -description



Inserts recognition results.




## -parameters




### -param pIInkRecoResult [in]

The <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> for the insertion which contains the recognition results and the collection of ink strokes for the insertion.


### -param locale [in]

The locale identifier of a specific culture for the input language of the recognizer used to produce alternates.


### -param fAlternateContainsAutoSpacingInformation [in]

Specifies whether the recognized text was generated with auto-spacing enabled on the recognized. <b>TRUE</b> if auto-spacing was enabled; otherwise, <b>FALSE</b>.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/67fcf19a-a864-40de-987f-406f18726a9f">IHandWrittenTextInsertion</a>
 

 

