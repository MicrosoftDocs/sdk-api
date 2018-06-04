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

# _NDR_USER_MARSHAL_INFO_LEVEL1 structure


## -description


The 
<b>NDR_USER_MARSHAL_INFO_LEVEL1</b> structure holds information about the state of an RPC call that can be passed to 
<a href="midl.wire_marshal">wire_marshal</a> and 
<a href="midl.user_marshal">user_marshal</a> helper functions.


## -struct-fields




### -field Buffer

Pointer to the beginning of the marshaling buffer available for use by the helper function. If no buffer is available, this field is null.


### -field BufferSize

Size, in bytes, of the marshaling buffer available for use by the helper function. If no buffer is available, <i>BufferSize</i> is zero.


### -field pfnAllocate

Function used by RPC to allocate memory for the application. An example of the use of this function is to create a node.


### -field pfnFree

Function used by RPC to free memory for the application. An example of the use of this function is to free a node.


### -field pRpcChannelBuffer

If the current call is for a COM interface, this member is a pointer to the channel buffer that RPC uses for the call. Otherwise, this member is null.


### -field Reserved

Reserved for future use.

