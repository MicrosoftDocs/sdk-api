---
UID: NS:rpcasync.tagRPC_EE_INFO_PARAM
title: tagRPC_EE_INFO_PARAM
author: windows-sdk-content
description: The RPC_EE_INFO_PARAM structure is used to store extended error information.
old-location: rpc\rpc_ee_info_param.htm
tech.root: rpc
ms.assetid: a201f8f3-6e74-4550-9738-d5415340994b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RPC_EE_INFO_PARAM, RPC_EE_INFO_PARAM structure [RPC], _rpc_rpc_ee_info_param, rpc.rpc_ee_info_param, rpcasync/RPC_EE_INFO_PARAM, tagRPC_EE_INFO_PARAM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_EE_INFO_PARAM
product: Windows
targetos: Windows
req.typenames: RPC_EE_INFO_PARAM
req.redist: 
---

# tagRPC_EE_INFO_PARAM structure


## -description


The 
<b>RPC_EE_INFO_PARAM</b> structure is used to store extended error information.


## -struct-fields




### -field ParameterType

Type of parameter being provided as extended error information. This value determines which union member(s) is used. Valid values are the following: 




<ul>
<li><b>eeptAnsiString</b> to specify an ANSI string, indicating the value is provided in <b>AnsiString</b>.</li>
<li><b>eeptUnicodeString</b> to specify a Unicode string, indicating the value is provided in <b>UnicodeString</b>.</li>
<li><b>eeptLongVal</b> to specify a LONG value, indicating the value is provided in <b>LVal</b>.</li>
<li><b>eeptShortVal</b> to specify a SHORT value, indicating the values is provided in <b>SVal</b>.</li>
<li><b>eeptPointerVal</b> to specify a pointer value, indicating the values is provided in <b>PVal</b>.</li>
<li><b>eeptBinary</b> is used by the RPC Runtime and should not be used or specified by applications.</li>
<li><b>eeptNone</b> indicates the parameter contained either a Unicode or ANSI string, but was truncated due to lack of memory or network fragment length limitations.</li>
</ul>

### -field u


### -field u.AnsiString

ANSI string representing the extended error information.


### -field u.UnicodeString

Unicode string representing the extended error information.


### -field u.LVal

Long value representing the extended error information.


### -field u.SVal

Short value representing the extended error information.


### -field u.PVal

ULONGLONG value representing the extended error information.


### -field u.BVal

Reserved.


## -remarks



The 
<b>RPC_EE_INFO_PARAM</b> structure is used in conjunction with the <b>RpcError</b>* functions to investigate and create extended RPC error information.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



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



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

