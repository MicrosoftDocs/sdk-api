---
UID: NF:rpcdce.UuidCreateNil
title: UuidCreateNil function
author: windows-sdk-content
description: The UuidCreateNil function creates a nil-valued UUID.
old-location: rpc\uuidcreatenil.htm
old-project: Rpc
ms.assetid: ee955482-e786-4478-bbaa-7c574ab1ecc5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UuidCreateNil, UuidCreateNil function [RPC], _rpc_uuidcreatenil, rpc.uuidcreatenil, rpcdce/UuidCreateNil
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - UuidCreateNil
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# UuidCreateNil function


## -description


The 
<b>UuidCreateNil</b> function creates a nil-valued <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


## -parameters




### -param NilUuid

Returns a nil-valued 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


## -returns



Returns RPC_S_OK.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>



<a href="https://msdn.microsoft.com/90b3cf6b-a15b-4f91-9ba2-0e43fe3374df">UuidFromString</a>



<a href="https://msdn.microsoft.com/49235b28-a0c5-4f69-9932-85350d7bcbb8">UuidToString</a>
 

 

