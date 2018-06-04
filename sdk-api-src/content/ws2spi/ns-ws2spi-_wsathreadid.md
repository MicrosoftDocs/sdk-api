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

# _WSATHREADID structure


## -description



			The 
<b>WSATHREADID</b> structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the 
<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a> function.


## -struct-fields




### -field ThreadHandle

Handle to the thread ID.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/4326547e-85e2-409c-9f36-aa013853dfd9">WPUQueueApc</a>



<a href="https://msdn.microsoft.com/098d85e3-8fe2-46c2-966d-deae4b12afd6"> WSPIoctl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566309">WSPRecv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566316">WSPSend</a>
 

 

