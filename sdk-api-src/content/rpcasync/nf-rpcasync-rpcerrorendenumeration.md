---
UID: NF:rpcasync.RpcErrorEndEnumeration
title: RpcErrorEndEnumeration function
author: windows-driver-content
description: The RpcErrorEndEnumeration function ends enumeration of extended error information and frees all resources allocated by RPC for the enumeration.
old-location: rpc\rpcerrorendenumeration.htm
old-project: Rpc
ms.assetid: 04da6e7d-bbdb-47d3-9924-604ddf56d177
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcErrorEndEnumeration, RpcErrorEndEnumeration function [RPC], _rpc_rpcerrorendenumeration, rpc.rpcerrorendenumeration, rpcasync/RpcErrorEndEnumeration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcErrorEndEnumeration
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcErrorEndEnumeration function


## -description


The 
<b>RpcErrorEndEnumeration</b> function ends enumeration of extended error information and frees all resources allocated by RPC for the enumeration.


## -parameters




### -param EnumHandle

Pointer to the enumeration handle.


## -returns



Successful completion returns RPC_S_OK. The 
<b>RpcErrorEndEnumeration</b> function call cannot fail unless its parameters are invalid.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcErrorEndEnumeration</b> function zeros out the enumeration handle to prevent further usage. If the CopyStrings option was not used during a previous call to the 
<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a> function, all non-empty <b>ComputerName</b> fields and <b>AnsiString</b> or <b>UnicodeString</b> values are invalid after this function is called.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

