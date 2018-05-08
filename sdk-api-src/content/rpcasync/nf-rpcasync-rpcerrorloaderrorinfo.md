---
UID: NF:rpcasync.RpcErrorLoadErrorInfo
title: RpcErrorLoadErrorInfo function
author: windows-driver-content
description: The RpcErrorLoadErrorInfo function converts a BLOB obtained by a call to RpcErrorSaveErrorInfo into extended error information.
old-location: rpc\rpcerrorloaderrorinfo.htm
old-project: Rpc
ms.assetid: cbd171ee-cef3-4880-a26d-81267cb813e9
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcErrorLoadErrorInfo, RpcErrorLoadErrorInfo function [RPC], _rpc_rpcerrorloaderrorinfo, rpc.rpcerrorloaderrorinfo, rpcasync/RpcErrorLoadErrorInfo
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
-	RpcErrorLoadErrorInfo
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcErrorLoadErrorInfo function


## -description


The 
<b>RpcErrorLoadErrorInfo</b> function converts a BLOB obtained by a call to 
<a href="https://msdn.microsoft.com/59a3ba71-10bd-47d1-91b0-eba5ffa5051b">RpcErrorSaveErrorInfo</a> into extended error information.


## -parameters




### -param ErrorBlob [in]

Pointer to the BLOB containing the error information.


### -param BlobSize [in]

Size of <i>ErrorBlob</i>, in bytes.


### -param EnumHandle [out]

Pointer to the enumeration handle associated with the extended error information.


## -returns



Successful completion returns RPC_S_OK. The <b>RpcErrorLoadInfo</b> function call can fail if not enough memory is available.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The BLOB pointed to in <i>ErrorBlob</i> remains the responsibility of the caller. The resulting enumeration is ready for enumeration. EnumHandle is subject to the same requirements of the <i>EnumHandle</i> parameter for 
<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>. Once enumeration is completed, resources allocated by the enumeration should be freed using the 
<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a>



<a href="https://msdn.microsoft.com/59a3ba71-10bd-47d1-91b0-eba5ffa5051b">RpcErrorSaveErrorInfo</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

