---
UID: NF:rpcasync.RpcErrorGetNextRecord
title: RpcErrorGetNextRecord function
author: windows-sdk-content
description: The RpcErrorGetNextRecord function retrieves the next extended error information record for an enumeration handle.
old-location: rpc\rpcerrorgetnextrecord.htm
tech.root: Rpc
ms.assetid: cc2d3aa0-2956-4710-ad31-a347d9ef9043
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RpcErrorGetNextRecord, RpcErrorGetNextRecord function [RPC], _rpc_rpcerrorgetnextrecord, rpc.rpcerrorgetnextrecord, rpcasync/RpcErrorGetNextRecord
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
 - RpcErrorGetNextRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcErrorGetNextRecord function


## -description


The 
<b>RpcErrorGetNextRecord</b> function retrieves the next extended error information record for an enumeration handle.


## -parameters




### -param EnumHandle [in]

Pointer to the enumeration handle, in the form of an 
<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a> structure. The structure must be allocated by the caller, and cannot be freed until the operation is complete. All members are ignored on input.


### -param CopyStrings [in]

Specifies whether the string fields in <i>ErrorInfo</i> are copied to the default system heap, at which point ownership of those buffers is transferred to the caller. 




TRUE indicates the strings are to be copied to the system heap.

FALSE indicates the strings in <i>ErrorInfo</i> point to internal RPC data structures; the caller cannot free or write to them, and they become invalid once the 
<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a> function is called.


### -param ErrorInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a> structure. See Remarks.


## -returns



If <i>CopyStrings</i> is false the function call cannot fail unless its parameters are invalid. When the last extended error record is retrieved, 
<b>RpcErrorGetNextRecord</b> returns RPC_S_OK. Any subsequent calls return RPC_S_ENTRY_NOT_FOUND.

Upon any error, the enumeration position is not advanced.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Upon input, the following fields must be set in <i>ErrorInfo</i>:

<ul>
<li><b>Version</b> must be set to RPC_EEINFO_VERSION.</li>
<li><b>NumberOfParameters</b> must be set to a value between zero and MaxNumberOfEEInfoParams. Callers are free to provide space for any number of parameters. If the number of parameters provided by the caller is smaller than the number of parameters in the extended error record, RPC_S_BUFFER_TOO_SMALL is returned.</li>
<li><b>Flags</b> must be zero, or <b>EEInfoUseFileTime</b> must be specified. If <b>Flags</b> is zero, the <b>SystemTime</b> member of the u union is used. If <b>EEInfoUseFileTime</b> is specified, the <b>FileTime</b> member of the u union is used.</li>
</ul>
Other fields of <i>ErrorInfo</i> are ignored on input.

Upon output, the fields in <i>ErrorInfo</i> are filled as follows:

<ul>
<li><b>Version</b> is unchanged.</li>
<li><b>ComputerName</b> is <b>NULL</b> if there is no computer name in the record, or a Unicode string if a computer name does exist in the extended error information record. If <b>NULL</b>, the last record with a computer name can be assumed, however, the computer name may have been dropped for insufficient memory. <b>ComputerName</b> is a non-qualified DNS name.</li>
<li><b>ProcessID</b> is the PID of the process where the record originated.</li>
<li><b>SystemTime</b> or <b>FileTime</b> is the time the record was generated, expressed in UCT, for the machine on which the record was generated. Either <b>FileTime</b> or <b>SystemTime</b> is valid, based on whether <b>EEInfoUseFileTime</b> is used.</li>
<li><b>GeneratingComponent</b> is the code for the generating component.</li>
<li><b>Status</b> is the status code for the record.</li>
<li><b>DetectionLocation</b> is the code for the detection location.</li>
<li><b>Flags</b> specifies whether records are missing. If one or more records is missing after the current record is missing, <b>EEInfoNextRecordsMissing</b> is set. If one or more record before the current record is missing, <b>EEInfoPreviousRecordsMissing</b> is set.</li>
<li><b>NumberOfParameters</b> specifies the true number of parameters. If the caller specified space for more parameters on input than there are in the record, this field contains the number of parameters used.</li>
<li><b>Parameters</b> is the actual parameters, provided as an array of 
<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a> structures with <b>NumberOfParameters</b> structures.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a>



<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

