---
UID: NS:rpcasync.tagRPC_EXTENDED_ERROR_INFO
title: RPC_EXTENDED_ERROR_INFO (rpcasync.h)
description: The RPC_EXTENDED_ERROR_INFO structure is used to store extended error information.
helpviewer_keywords: ["RPC_EXTENDED_ERROR_INFO","RPC_EXTENDED_ERROR_INFO structure [RPC]","_rpc_rpc_extended_error_info","rpc.rpc_extended_error_info","rpcasync/RPC_EXTENDED_ERROR_INFO"]
old-location: rpc\rpc_extended_error_info.htm
tech.root: Rpc
ms.assetid: 1e906192-c9f1-41c2-bf7f-9967a3d0e1d3
ms.date: 12/05/2018
ms.keywords: RPC_EXTENDED_ERROR_INFO, RPC_EXTENDED_ERROR_INFO structure [RPC], _rpc_rpc_extended_error_info, rpc.rpc_extended_error_info, rpcasync/RPC_EXTENDED_ERROR_INFO
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
targetos: Windows
req.typenames: RPC_EXTENDED_ERROR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPC_EXTENDED_ERROR_INFO
 - rpcasync/tagRPC_EXTENDED_ERROR_INFO
 - RPC_EXTENDED_ERROR_INFO
 - rpcasync/RPC_EXTENDED_ERROR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_EXTENDED_ERROR_INFO
---

# RPC_EXTENDED_ERROR_INFO structure


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
<a href="/windows/desktop/Rpc/extended-error-information-detection-locations">Extended Error Information Detection Locations</a> for valid locations.

### -field Flags

On input, specifies whether <b>SystemTime</b> or <b>FileTime</b> is used. Set to zero to use <b>SystemTime</b>, or EEInfoUseFileTime to use <b>FileTime</b>. 




On output, specifies whether records are missing. If a record is missing after the current record, <b>Flags</b> is set to EEInfoNextRecordsMissing. If a record is missing before the current record, <b>Flags</b> is set to EEInfoPreviousRecordsMissing.

### -field NumberOfParameters

Number of parameters in the <b>Parameters</b> member.

### -field Parameters

Array of 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_ee_info_param">RPC_EE_INFO_PARAM</a> structures containing the extended error information.

## -remarks

On input, the caller fills in only the <b>Version</b> and <b>Flags</b> members of the 
<b>RPC_EXTENDED_ERROR_INFO</b> structure. All other members are filled upon output by RPC.

The 
<b>RPC_EXTENDED_ERROR_INFO</b> structure is used in conjunction with the <b>RpcError</b>* functions to investigate and create extended RPC error information.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_ee_info_param">RPC_EE_INFO_PARAM</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorclearinformation">RpcErrorClearInformation</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorendenumeration">RpcErrorEndEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnumberofrecords">RpcErrorGetNumberOfRecords</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorloaderrorinfo">RpcErrorLoadErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorresetenumeration">RpcErrorResetEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo">RpcErrorSaveErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>