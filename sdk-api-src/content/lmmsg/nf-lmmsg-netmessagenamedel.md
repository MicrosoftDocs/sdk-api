---
UID: NF:lmmsg.NetMessageNameDel
title: NetMessageNameDel function
author: windows-sdk-content
description: The NetMessageNameDel function deletes a message alias in the message name table. The function requires that the messenger service be started.
old-location: netmgmt\netmessagenamedel.htm
old-project: NetMgmt
ms.assetid: 6d6c65ee-f53e-4a24-b8c0-50faa76af640
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: NetMessageNameDel, NetMessageNameDel function [Network Management], _win32_netmessagenamedel, lmmsg/NetMessageNameDel, netmgmt.netmessagenamedel
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: NETSETUP_PROVISIONING_PARAMS, *PNETSETUP_PROVISIONING_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetMessageNameDel
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/9face737-3472-4a53-97b6-e861a60ee96a">Message
		  Functions</a>



<a href="https://msdn.microsoft.com/5330e883-5439-46af-b4ae-b0926feadb70">NetMessageNameAdd</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

