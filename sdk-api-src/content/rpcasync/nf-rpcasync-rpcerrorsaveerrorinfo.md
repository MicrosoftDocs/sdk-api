---
UID: NF:rpcasync.RpcErrorSaveErrorInfo
title: RpcErrorSaveErrorInfo function
author: windows-sdk-content
description: The RpcErrorSaveErrorInfo function returns all error information for an enumeration handle as a BLOB.
old-location: rpc\rpcerrorsaveerrorinfo.htm
tech.root: Rpc
ms.assetid: 59a3ba71-10bd-47d1-91b0-eba5ffa5051b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RpcErrorSaveErrorInfo, RpcErrorSaveErrorInfo function [RPC], _rpc_rpcerrorsaveerrorinfo, rpc.rpcerrorsaveerrorinfo, rpcasync/RpcErrorSaveErrorInfo
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
 - RpcErrorSaveErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcErrorSaveErrorInfo function


## -description


The 
<b>RpcErrorSaveErrorInfo</b> function returns all error information for an enumeration handle as a BLOB.


## -parameters




### -param EnumHandle [in]

Pointer to the enumeration handle.


### -param ErrorBlob [out]

Pointer to the BLOB containing the error information.


### -param BlobSize [out]

Size of <i>ErrorBlob</i>, in bytes.


## -returns



Successful completion returns RPC_S_OK. The 
<b>RpcErrorSaveErrorInfo</b> function call may fail if not enough memory is available.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The BLOB is allocated on the system heap, and the caller is the owner of the buffer. The block allocated on the system heap may be larger than <i>BlobSize</i>, but only <i>BlobSize</i> is used. The 
<b>RpcErrorSaveErrorInfo</b> function saves the entire chain of extended error information records associated with the enumeration handle, regardless of cursor position, and does not change the cursor position for the enumeration.

The BLOB may be saved and later retrieved using the 
<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

