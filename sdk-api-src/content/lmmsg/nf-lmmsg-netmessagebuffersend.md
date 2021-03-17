---
UID: NF:lmmsg.NetMessageBufferSend
title: NetMessageBufferSend function (lmmsg.h)
description: The NetMessageBufferSend function sends a buffer of information to a registered message alias.
helpviewer_keywords: ["NetMessageBufferSend","NetMessageBufferSend function [Network Management]","_win32_netmessagebuffersend","lmmsg/NetMessageBufferSend","netmgmt.netmessagebuffersend"]
old-location: netmgmt\netmessagebuffersend.htm
tech.root: NetMgmt
ms.assetid: d1b9bebd-52e9-4b5f-97fb-e2a98aaff6b7
ms.date: 12/05/2018
ms.keywords: NetMessageBufferSend, NetMessageBufferSend function [Network Management], _win32_netmessagebuffersend, lmmsg/NetMessageBufferSend, netmgmt.netmessagebuffersend
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
 - NetMessageBufferSend
 - lmmsg/NetMessageBufferSend
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
 - NetMessageBufferSend
---

# NetMessageBufferSend function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the messenger service is not supported.]

The 
				<b>NetMessageBufferSend</b> function sends a buffer of information to a registered message alias.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param msgname [in]

Pointer to a constant string that specifies the message alias to which the message buffer should be sent.

### -param fromname [in]

Pointer to a constant string specifying who the message is from. If this parameter is <b>NULL</b>, the message is sent from the local computer name.

### -param buf [in]

Pointer to a buffer that contains the message text. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param buflen [in]

Specifies a value that contains the length, in bytes, of the message text pointed to by the <i>buf</i> parameter.

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
<dt><b>NERR_NameNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

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
</table>

## -remarks

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the securable object. The default ACL permits only Domain Admins and Account Operators to call this function. On a member server or workstation, only Administrators and Server Operators can call this function. For more information, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs and ACEs, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

## -see-also

<a href="/windows/desktop/NetMgmt/message-functions">Message
		  Functions</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenameadd">NetMessageNameAdd</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamedel">NetMessageNameDel</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenameenum">NetMessageNameEnum</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamegetinfo">NetMessageNameGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>