---
UID: NF:lmmsg.NetMessageNameAdd
title: NetMessageNameAdd function (lmmsg.h)
description: The NetMessageNameAdd function registers a message alias in the message name table. The function requires that the messenger service be started.
helpviewer_keywords: ["NetMessageNameAdd","NetMessageNameAdd function [Network Management]","_win32_netmessagenameadd","lmmsg/NetMessageNameAdd","netmgmt.netmessagenameadd"]
old-location: netmgmt\netmessagenameadd.htm
tech.root: NetMgmt
ms.assetid: 5330e883-5439-46af-b4ae-b0926feadb70
ms.date: 12/05/2018
ms.keywords: NetMessageNameAdd, NetMessageNameAdd function [Network Management], _win32_netmessagenameadd, lmmsg/NetMessageNameAdd, netmgmt.netmessagenameadd
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
 - NetMessageNameAdd
 - lmmsg/NetMessageNameAdd
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
 - NetMessageNameAdd
---

# NetMessageNameAdd function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the messenger service is not supported.]

The
				<b>NetMessageNameAdd</b> function registers a message alias in the message name table. The function requires that the messenger service be started.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param msgname [in]

Pointer to a constant string that specifies the message alias to add. The string cannot be more than 15 characters long.

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
<dt><b>NERR_AlreadyExists</b></dt>
</dl>
</td>
<td width="60%">
The message alias already exists on this computer. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_DuplicateName</b></dt>
</dl>
</td>
<td width="60%">
The name specified is already in use as a message alias on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NetworkError</b></dt>
</dl>
</td>
<td width="60%">
A general failure occurred in the network hardware.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_TooManyNames</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of message aliases has been exceeded.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators local group can successfully execute the 
<b>NetMessageNameAdd</b> function on a remote server.

The forward action flag is no longer a parameter to the LAN Manager 2.<i>x</i><b>NetMessageNameAdd</b> function because message forwarding is no longer supported. If the 
<b>NetMessageNameAdd</b> function detects that a forwarded version of <i>msgname</i> exists on the network, the function will fail with error NERR_Already_Exists.

## -see-also

<a href="/windows/desktop/NetMgmt/message-functions">Message
		  Functions</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamedel">NetMessageNameDel</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>