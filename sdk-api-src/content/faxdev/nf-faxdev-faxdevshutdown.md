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

# FaxDevShutdown function


## -description


The fax service calls the <b>FaxDevShutdown</b> function to notify the fax service provider (FSP) that the service is about to unload the FSP's DLL. <b>FaxDevShutdown</b> releases the global resources allocated by the <a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a> function.

Exporting the <b>FaxDevShutdown</b> function is optional.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the function succeeds, the return value is S_OK.

If the function fails, the return value is E_FAIL.




## -remarks



The fax service always unloads the FSP's DLL, even if the FSP returns failure in response to this function.




## -see-also




<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/74c4ebad-c1a5-48a4-9ced-548ab21b3c3c">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

