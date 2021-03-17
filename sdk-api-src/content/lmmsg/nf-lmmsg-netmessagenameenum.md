---
UID: NF:lmmsg.NetMessageNameEnum
title: NetMessageNameEnum function (lmmsg.h)
description: The NetMessageNameEnum function lists the message aliases that receive messages on a specified computer. The function requires that the messenger service be started.
helpviewer_keywords: ["0","1","NetMessageNameEnum","NetMessageNameEnum function [Network Management]","_win32_netmessagenameenum","lmmsg/NetMessageNameEnum","netmgmt.netmessagenameenum"]
old-location: netmgmt\netmessagenameenum.htm
tech.root: NetMgmt
ms.assetid: fc1b11e6-294d-47d3-8c63-bee80b5a8581
ms.date: 12/05/2018
ms.keywords: 0, 1, NetMessageNameEnum, NetMessageNameEnum function [Network Management], _win32_netmessagenameenum, lmmsg/NetMessageNameEnum, netmgmt.netmessagenameenum
req.header: lmmsg.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetMessageNameEnum
 - lmmsg/NetMessageNameEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetMessageNameEnum
---

# NetMessageNameEnum function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the messenger service is not supported.]

The
				<b>NetMessageNameEnum</b> function lists the message aliases that receive messages on a specified computer. The function requires that the messenger service be started.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Return message aliases. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmmsg/ns-lmmsg-msg_info_0">MSG_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return message aliases. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmmsg/ns-lmmsg-msg_info_1">MSG_INFO_1</a> structures. This level exists only for compatibility. Message forwarding is not supported.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

Specifies the preferred maximum length of the returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.

### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing message alias search. The handle should be zero on the first call and left unchanged for subsequent calls. If <i>resume_handle</i> is <b>NULL</b>, no resume handle is stored.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the appropriate
        access to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This request is not supported. This error is returned on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is too small.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators local group can successfully execute the 
<b>NetMessageNameEnum</b> function on a remote server.

To retrieve information about a particular message alias in the message name table, you can call the 
<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamegetinfo">NetMessageNameGetInfo</a> function.

## -see-also

<a href="/windows/desktop/api/lmmsg/ns-lmmsg-msg_info_0">MSG_INFO_0</a>



<a href="/windows/desktop/api/lmmsg/ns-lmmsg-msg_info_1">MSG_INFO_1</a>



<a href="/windows/desktop/NetMgmt/message-functions">Message
		  Functions</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamegetinfo">NetMessageNameGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>