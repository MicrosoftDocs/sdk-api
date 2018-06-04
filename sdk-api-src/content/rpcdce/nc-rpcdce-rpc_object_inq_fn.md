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

# RPC_OBJECT_INQ_FN callback function


## -description


The 
<b>RPC_OBJECT_INQ_FN</b> function is a prototype for a function that facilitates replacement of the default object UUID to type UUID mapping.


## -parameters




### -param *ObjectUuid

Pointer to the variable that specifies the object 
<a href="midl.uuid">UUID</a> that is to be mapped to a type UUID.


### -param *TypeUuid

Pointer to the address of the variable that is to contain the type UUID derived from the object UUID. The type UUID is returned by the function.


### -param *Status

Pointer to a return value for the function.


## -returns



This callback function does not return a value.




## -remarks



You can replace the default mapping function that maps object UUIDs to type UUIDs by calling 
<a href="https://msdn.microsoft.com/358d3ab3-df16-486b-aeac-56a0ffc78272">RpcObjectSetInqFn</a> and supplying a pointer to a function of type RPC_OBJECT_INQ_FN. The supplied function must match the function prototype specified by the type definition: a function with three parameters and the function return value of void.




## -see-also




<a href="https://msdn.microsoft.com/358d3ab3-df16-486b-aeac-56a0ffc78272">RpcObjectSetInqFn</a>
 

 

