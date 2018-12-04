---
UID: NF:rpcasync.RpcErrorGetNumberOfRecords
title: RpcErrorGetNumberOfRecords function
author: windows-sdk-content
description: The RpcErrorGetNumberOfRecords function returns the number of records in the extended error information.
old-location: rpc\rpcerrorgetnumberofrecords.htm
tech.root: rpc
ms.assetid: 1b498cc8-9ee5-47bd-a484-33bf1c89413c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RpcErrorGetNumberOfRecords, RpcErrorGetNumberOfRecords function [RPC], _rpc_rpcerrorgetnumberofrecords, rpc.rpcerrorgetnumberofrecords, rpcasync/RpcErrorGetNumberOfRecords
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
 - RpcErrorGetNumberOfRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcErrorGetNumberOfRecords function


## -description


The 
<b>RpcErrorGetNumberOfRecords</b> function returns the number of records in the extended error information.


## -parameters




### -param EnumHandle [in]

Pointer to the enumeration handle.


### -param Records [out]

Number of records for the extended error information.


## -returns



Successful completion returns RPC_S_OK. The <b>RpcErrorGetNumberOfRecords</b> function call cannot fail unless its parameters are invalid.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcErrorGetNumberOfRecords</b> function returns the total number of records in the extended error information, not the number of records from the current cursor location.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

