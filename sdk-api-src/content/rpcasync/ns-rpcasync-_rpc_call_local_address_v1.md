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

# _RPC_CALL_LOCAL_ADDRESS_V1 structure


## -description


The <b>RPC_CALL_LOCAL_ADDRESS_V1</b> structure  contains information about the local address on which a call was made.


## -struct-fields




### -field Version

Version of the <b>RPC_CALL_LOCAL_ADDRESS</b> structure. For this structure, this value must be set to 1.


### -field Buffer

Pointer to a user-supplied opaque data block that contains the local address.


### -field BufferSize

On input, this member contains the size of the buffer pointed to by the <b>Buffer</b> member, in bytes. On output, it contains the actual number of bytes written to buffer. For example, if the buffer is allocated a size of 8 bytes, but the local address written to it is 4, this parameter will specify 8 on input and contain 4 on output.


### -field AddressFormat


<a href="https://msdn.microsoft.com/c05610ba-6b00-45e4-b28f-9ce288d08df8">RpcLocalAddressFormat</a> enumeration values that specifies the format of the local address written to <b>Buffer</b>. For this version of the structure, only IPv4 and IPv6 addresses  are supported; if another is specified, RPC_S_CANNOT_SUPPORT is returned.


## -see-also




<a href="https://msdn.microsoft.com/eccc4b78-19f8-415f-bd0f-b1f9f454435e">RPC_CALL_ATTRIBUTES_V2</a>
 

 

