---
UID: NS:rpcasync.tagRPC_EXTENDED_ERROR_INFO
title: tagRPC_EXTENDED_ERROR_INFO
author: windows-sdk-content
description: The RPC_EXTENDED_ERROR_INFO structure is used to store extended error information.
old-location: rpc\rpc_extended_error_info.htm
tech.root: rpc
ms.assetid: 1e906192-c9f1-41c2-bf7f-9967a3d0e1d3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RPC_EXTENDED_ERROR_INFO, RPC_EXTENDED_ERROR_INFO structure [RPC], _rpc_rpc_extended_error_info, rpc.rpc_extended_error_info, rpcasync/RPC_EXTENDED_ERROR_INFO, tagRPC_EXTENDED_ERROR_INFO
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
 - RPC_EXTENDED_ERROR_INFO
product: Windows
targetos: Windows
req.typenames: RPC_EXTENDED_ERROR_INFO
req.redist: 
---

# tagRPC_EXTENDED_ERROR_INFO structure


## -description


The 
<b>RPC_EXTENDED_ERROR_INFO</b> structure is used to store extended error information.


## -struct-fields




### -field Version

Version of the structure. Must be RPC_EEINFO_VERSION.


### -field ComputerName

Non-qualified DNS name, expressed in Unicode.


### -field ProcessID

Process identifier for the offending error event.


### -field u


### -field u.SystemTime

Time the record was generated, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds. Either <b>FileTime</b> or <b>SystemTime</b> is valid, based on whether <b>EEInfoUseFileTime</b> is used in the <b>Flags</b> member.


### -field u.FileTime

Time the record was generated, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds. Either <b>FileTime</b> or <b>SystemTime</b> is valid, based on whether <b>EEInfoUseFileTime</b> is used in the <b>Flags</b> member..


### -field u.KernelTime

 


### -field GeneratingComponent

Code for the component that generated the error.


### -field Status

Status code for the error.


### -field DetectionLocation

Code for the detection location. See 
<a href="https://msdn.microsoft.com/73c4d044-363f-4bf5-a8ea-37d8a227183a">Extended Error Information Detection Locations</a> for valid locations.


### -field Flags

On input, specifies whether <b>SystemTime</b> or <b>FileTime</b> is used. Set to zero to use <b>SystemTime</b>, or EEInfoUseFileTime to use <b>FileTime</b>. 




On output, specifies whether records are missing. If a record is missing after the current record, <b>Flags</b> is set to EEInfoNextRecordsMissing. If a record is missing before the current record, <b>Flags</b> is set to EEInfoPreviousRecordsMissing.


### -field NumberOfParameters

Number of parameters in the <b>Parameters</b> member.


### -field Parameters

Array of 
<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a> structures containing the extended error information.


## -remarks



On input, the caller fills in only the <b>Version</b> and <b>Flags</b> members of the 
<b>RPC_EXTENDED_ERROR_INFO</b> structure. All other members are filled upon output by RPC.

The 
<b>RPC_EXTENDED_ERROR_INFO</b> structure is used in conjunction with the <b>RpcError</b>* functions to investigate and create extended RPC error information.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a>



<a href="https://msdn.microsoft.com/ff96904c-285d-4d39-af3b-bf295c29e62f">RpcErrorClearInformation</a>



<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/1b498cc8-9ee5-47bd-a484-33bf1c89413c">RpcErrorGetNumberOfRecords</a>



<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a>



<a href="https://msdn.microsoft.com/fb41b923-7fd3-4058-9f5f-df4018d9b872">RpcErrorResetEnumeration</a>



<a href="https://msdn.microsoft.com/59a3ba71-10bd-47d1-91b0-eba5ffa5051b">RpcErrorSaveErrorInfo</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

