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

# AuthzInitializeRemoteResourceManager function


## -description


The <b>AuthzInitializeRemoteResourceManager</b> function allocates and initializes a remote resource manager. The caller can use the resulting handle to make AuthZ calls over RPC to a remote instance of the resource manager configured on a server.


## -parameters




### -param pRpcInitInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/6859A0CB-F88E-42BF-A350-293D28E908DD">AUTHZ_RPC_INIT_INFO_CLIENT</a> structure containing the initial information needed to configure the connection.


### -param phAuthzResourceManager [out]

A handle to the resource manager. When you have finished using the handle, free it by calling the <a href="https://msdn.microsoft.com/8b716368-8d81-4c62-9086-0976b39bbcf8">AuthzFreeResourceManager</a> function.


## -returns




						If the function succeeds, the function returns <b>TRUE</b>. 

If the function fails, it returns <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



