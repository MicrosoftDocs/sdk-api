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

# WsFreeServiceProxy function


## -description


Releases the memory associated with  a Service Proxy resource.
            


## -parameters




### -param serviceProxy [in]

A pointer to the <b>Service Proxy</b> to release.  The pointer must reference a valid <a href="https://msdn.microsoft.com/623766ae-fe82-40f9-93c8-e78fe48bc6d1">WS_SERVICE_PROXY</a> object
                    returned by <a href="https://msdn.microsoft.com/9215684b-979e-48ad-b4ee-2ae1db1e3034">WsCreateServiceProxy</a>. The referenced value may not be <b>NULL</b>.
                


## -returns



This function does not return a value.




## -remarks




               For details of when it is allowed to call this function, see <a href="https://msdn.microsoft.com/e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc">Service Proxy</a> .
            



