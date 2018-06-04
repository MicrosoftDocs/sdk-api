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

# FaxExtFreeBuffer function


## -description


The <b>FaxExtFreeBuffer</b> callback function deallocates memory previously allocated by a successful call to the <a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a> function.


## -parameters




### -param lpvBuffer

Type: <b>LPVOID</b>

Pointer to the data retrieved by a successful call to the <a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a> function.


## -returns



None.




## -remarks



When the fax extension calls this fax service callback function, it must use the function pointer exposed by the fax service when the service calls the <a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a> function.

The fax service passes a pointer to the <b>FaxExtFreeBuffer</b> callback function when the fax service calls the <a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a> function. The PFAX_EXT_FREE_BUFFER data type is a pointer to a <b>FaxExtFreeBuffer</b> function.




## -see-also




<a href="https://msdn.microsoft.com/164c3919-49ad-4d29-a44d-27985c877268">FaxExtGetData</a>



<a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a>
 

 

