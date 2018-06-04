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

# DsReplicaVerifyObjectsW function


## -description


The <b>DsReplicaVerifyObjects</b> function verifies all objects for a naming context with a source.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a>, 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a>, or <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a> function.


### -param NameContext [in]

Pointer to a null-terminated string that contains the distinguished name of the naming context.


### -param pUuidDsaSrc [in]

Pointer to a <b>UUID</b> value that contains the <b>objectGuid</b> of the directory system agent object.


### -param ulOptions [in]

Contains a set of flags that modify the behavior of the function. This can be zero or the following value.



#### DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.


##### - ulOptions.DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error otherwise. Possible error values include the following.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>
 

 

