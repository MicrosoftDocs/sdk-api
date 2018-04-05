---
UID: NF:rpcdce.UuidHash
title: UuidHash function
author: windows-driver-content
description: An application calls the UuidHash function to generate a hash value for a specified UUID.
old-location: rpc\uuidhash.htm
old-project: Rpc
ms.assetid: e96fafa6-1c10-42c1-8d85-5e338899411d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UuidHash, UuidHash function [RPC], _rpc_uuidhash, rpc.uuidhash, rpcdce/UuidHash
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	UuidHash
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# UuidHash function


## -description



			An application calls the 
<b>UuidHash</b> function to generate a hash value for a specified <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


## -parameters




### -param Uuid


<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> for which a hash value is created.


### -param Status

Returns RPC_S_OK.


## -returns



<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls 
<b>UuidHash</b> to generate a hash value for a specified <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>. The hash value returned is implementation dependent and may vary from implementation to implementation.




## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>
 

 

