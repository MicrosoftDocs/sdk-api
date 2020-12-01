---
UID: NF:lmmsg.NetMessageNameDel
title: NetMessageNameDel function (lmmsg.h)
description: The NetMessageNameDel function deletes a message alias in the message name table. The function requires that the messenger service be started.
helpviewer_keywords: ["NetMessageNameDel","NetMessageNameDel function [Network Management]","_win32_netmessagenamedel","lmmsg/NetMessageNameDel","netmgmt.netmessagenamedel"]
old-location: netmgmt\netmessagenamedel.htm
tech.root: NetMgmt
ms.assetid: 6d6c65ee-f53e-4a24-b8c0-50faa76af640
ms.date: 12/05/2018
ms.keywords: NetMessageNameDel, NetMessageNameDel function [Network Management], _win32_netmessagenamedel, lmmsg/NetMessageNameDel, netmgmt.netmessagenamedel
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
 - NetMessageNameDel
 - lmmsg/NetMessageNameDel
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
 - NetMessageNameDel
---

# NetMessageNameDel function


## -description

<p class="CCE_Message">[This function is not supported as of Windows Vista because the messenger service is not supported.]

The
				<b>NetMessageNameDel</b> function deletes a message alias in the message name table. The function requires that the messenger service be started.

## -parameters

### -param servername [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param msgname [in]

Pointer to a constant string that specifies the message alias to delete. The string cannot be more than 15 characters long.

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
<dt><b>NERR_DelComputerName</b></dt>
</dl>
</td>
<td width="60%">
A message alias that is also a computer name cannot be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_IncompleteDel</b></dt>
</dl>
</td>
<td width="60%">
The message alias was not successfully deleted from all networks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NameInUse</b></dt>
</dl>
</td>
<td width="60%">
The message alias is currently in use. Try again later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NotLocalName</b></dt>
</dl>
</td>
<td width="60%">
The message alias is not on the local computer.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators local group can successfully execute the 
<b>NetMessageNameDel</b> function on a remote server.

## -see-also

<a href="/windows/desktop/NetMgmt/message-functions">Message
		  Functions</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenameadd">NetMessageNameAdd</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>