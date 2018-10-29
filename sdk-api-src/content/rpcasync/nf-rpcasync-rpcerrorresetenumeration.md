---
UID: NF:rpcasync.RpcErrorResetEnumeration
title: RpcErrorResetEnumeration function
author: windows-sdk-content
description: The RpcErrorResetEnumeration function resets an enumeration cursor for any in-process enumeration, resetting the process such that a subsequent call to the RpcErrorGetNextRecord retrieves the first extended error information record.
old-location: rpc\rpcerrorresetenumeration.htm
tech.root: Rpc
ms.assetid: fb41b923-7fd3-4058-9f5f-df4018d9b872
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcErrorResetEnumeration, RpcErrorResetEnumeration function [RPC], _rpc_rpcerrorresetenumeration, rpc.rpcerrorresetenumeration, rpcasync/RpcErrorResetEnumeration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcErrorResetEnumeration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcErrorResetEnumeration function


## -description


The 
<b>RpcErrorResetEnumeration</b> function resets an enumeration cursor for any in-process enumeration, resetting the process such that a subsequent call to the 
<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a> retrieves the first extended error information record.


## -parameters




### -param EnumHandle

Pointer to the enumeration handle.


## -returns



Successful completion returns RPC_S_OK. The 
<b>RpcErrorResetEnumeration</b> function call cannot fail unless its parameters are invalid.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcErrorResetEnumeration</b> function call can reset an enumeration of extended error information even if the 
<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a> function reaches the end of enumerations and returns RPC_S_SNTRY_NOT_FOUND.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

