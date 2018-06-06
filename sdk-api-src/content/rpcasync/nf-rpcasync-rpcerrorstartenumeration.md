---
UID: NF:rpcasync.RpcErrorStartEnumeration
title: RpcErrorStartEnumeration function
author: windows-sdk-content
description: The RpcErrorStartEnumeration function begins enumeration of extended error information.
old-location: rpc\rpcerrorstartenumeration.htm
old-project: Rpc
ms.assetid: 56c61902-4b34-4d92-b352-cd1837754aa3
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcErrorStartEnumeration, RpcErrorStartEnumeration function [RPC], _rpc_rpcerrorstartenumeration, rpc.rpcerrorstartenumeration, rpcasync/RpcErrorStartEnumeration
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcErrorStartEnumeration
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcErrorStartEnumeration function


## -description


The 
<b>RpcErrorStartEnumeration</b> function begins enumeration of extended error information.


## -parameters




### -param EnumHandle

Pointer to the enumeration handle, in the form of an 
<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a> structure. The structure must be allocated by the caller, and cannot be freed until the operation is complete. All members are ignored on input.


## -returns



Successful completion returns RPC_S_OK.

Returns RPC_S_ENTRY_NOT_FOUND if no extended error information is on the thread. If an enumeration is in progress, starting a second enumeration starts from the beginning.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The RpcErrorStartEnumeration function call should be made immediately after the call that returned the error. Otherwise, extended error information may be overwritten by subsequent calls. Enumeration handles must be freed with the RpcErrorEndEnumeration function.

Once 
<b>RpcErrorStartEnumeration</b> is called, it is safe to use the enumeration handle from a different thread. The 
<b>RpcErrorStartEnumeration</b> function takes a snapshot of the extended error information, and the returning enumeration handle operates on the snapshot. However, enumeration functions are not synchronized between threads by RPC, and so the caller is responsible for doing so. Subsequent calls to 
<b>RpcErrorStartEnumeration</b> begins a new enumeration, and does not create a second enumeration for the same extended error information.

The RpcErrorStartEnumeration function may fail if there is not enough memory to begin the enumeration. The enumeration handle can be passed only to <b>RpcError</b>* functions, and cannot be used with other functions, such as <b>DuplicateHandle</b>.

Advancing the enumeration pointer on one enumeration has no effect on independently started enumerations.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a>



<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a>



<a href="https://msdn.microsoft.com/ff96904c-285d-4d39-af3b-bf295c29e62f">RpcErrorClearInformation</a>



<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/1b498cc8-9ee5-47bd-a484-33bf1c89413c">RpcErrorGetNumberOfRecords</a>



<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a>



<a href="https://msdn.microsoft.com/fb41b923-7fd3-4058-9f5f-df4018d9b872">RpcErrorResetEnumeration</a>



<a href="https://msdn.microsoft.com/59a3ba71-10bd-47d1-91b0-eba5ffa5051b">RpcErrorSaveErrorInfo</a>
 

 

