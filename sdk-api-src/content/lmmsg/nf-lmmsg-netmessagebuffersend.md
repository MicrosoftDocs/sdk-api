---
UID: NF:lmmsg.NetMessageBufferSend
title: NetMessageBufferSend function (lmmsg.h)
author: windows-sdk-content
description: The NetMessageBufferSend function sends a buffer of information to a registered message alias.
old-location: netmgmt\netmessagebuffersend.htm
tech.root: NetMgmt
ms.assetid: d1b9bebd-52e9-4b5f-97fb-e2a98aaff6b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetMessageBufferSend, NetMessageBufferSend function [Network Management], _win32_netmessagebuffersend, lmmsg/NetMessageBufferSend, netmgmt.netmessagebuffersend
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetMessageBufferSend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


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
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs and ACEs, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/9face737-3472-4a53-97b6-e861a60ee96a">Message
		  Functions</a>



<a href="https://msdn.microsoft.com/5330e883-5439-46af-b4ae-b0926feadb70">NetMessageNameAdd</a>



<a href="https://msdn.microsoft.com/6d6c65ee-f53e-4a24-b8c0-50faa76af640">NetMessageNameDel</a>



<a href="https://msdn.microsoft.com/fc1b11e6-294d-47d3-8c63-bee80b5a8581">NetMessageNameEnum</a>



<a href="https://msdn.microsoft.com/72129865-2aee-41d5-8a89-53bb815a7f63">NetMessageNameGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

