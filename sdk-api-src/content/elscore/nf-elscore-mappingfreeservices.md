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

# MappingFreeServices function


## -description


Frees memory and resources allocated for the application to interact with one or more ELS services. The memory and resources are allocated in an application call to <a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a>.


## -parameters




### -param pServiceInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a> structures containing service descriptions retrieved by a prior call to <a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a>. This parameter cannot be set to <b>NULL</b>. 


## -returns



Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.




## -remarks



<div class="alert"><b>Caution</b>  Services should not be freed before freeing the property bags produced by those services.</div>
<div> </div>
Since all services currently run in the application process, the ELS platform does not unload the service DLLs when the services are released. The operating system unloads the DLLs automatically when the application terminates.




## -see-also




<a href="https://msdn.microsoft.com/526e51c7-9ff2-4590-b092-172f4942ce8e">Enumerating and Freeing Services</a>



<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a>
 

 

