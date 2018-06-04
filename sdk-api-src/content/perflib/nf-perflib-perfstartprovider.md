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

# PerfStartProvider function


## -description


Registers the provider.


## -parameters




### -param ProviderGuid [in]

GUID that uniquely identifies the provider. The <b>providerGuid</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element specifies the GUID.


### -param ControlCallback [in, optional]


<a href="https://msdn.microsoft.com/0f771ab7-af42-481b-b2da-20dcdf49b82b">ControlCallback</a> function that PERFLIB calls to notify you of consumer requests, such as a request to add or remove counters from the query. This parameter is set if the <b>callback</b> attribute of the <b>counters</b> element is "custom"; otherwise, <b>NULL</b>. 


### -param phProvider [out]

Handle to the provider. You must call <a href="https://msdn.microsoft.com/4b31f88b-cadc-4bee-bdea-9079cc14c140">PerfStopProvider</a> to release resources associated with the handle.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/edcf8df3-0f6d-4849-b41d-270509499b8e">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.




## -see-also




<a href="https://msdn.microsoft.com/4b31f88b-cadc-4bee-bdea-9079cc14c140">PerfStopProvider</a>
 

 

