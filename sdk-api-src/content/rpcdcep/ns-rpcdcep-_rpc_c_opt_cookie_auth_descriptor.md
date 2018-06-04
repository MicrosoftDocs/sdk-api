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

# _RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure


## -description


The <b>RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR</b> structure contains a cookie that is inserted into the header of RPC/HTTP traffic. This cookie can be used for authentication or for load balancing. When used for authentication, <a href="https://msdn.microsoft.com/7e57c087-53e4-443d-9227-21d9eb3cc71f">RPC_S_COOKIE_AUTH_FAILED</a>  is returned from an RPC call if cookie authentication fails. There are no specific error messages when used for load balancing.


## -struct-fields




### -field BufferSize

The length, in bytes, of <b>Buffer</b>.


### -field Buffer

A null-terminated string that contains the cookie.


## -remarks



A pointer to this structure is passed as the OptionValue when making a call to <a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>  with <a href="https://msdn.microsoft.com/ff88e05d-b9f3-42ef-a44f-fee9261832c8">RPC_C_OPT_COOKIE_AUTH</a>  as the option.



