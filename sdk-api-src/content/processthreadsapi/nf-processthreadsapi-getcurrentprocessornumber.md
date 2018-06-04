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

# GetCurrentProcessorNumber function


## -description


Retrieves the number of the processor the current thread was running on during the call to this function.


## -parameters






## -returns



The function returns the current processor number.




## -remarks



This function is used to provide information for estimating process performance.

On systems with more than 64 logical processors, the <b>GetCurrentProcessorNumber</b> function returns the processor number within the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> to which the logical processor is assigned. Use the <a href="https://msdn.microsoft.com/46c3d3f7-7a82-40d3-8a9e-0f8d0df534f3">GetCurrentProcessorNumberEx</a> function to retrieve the processor group and number of the current processor.




## -see-also




<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

