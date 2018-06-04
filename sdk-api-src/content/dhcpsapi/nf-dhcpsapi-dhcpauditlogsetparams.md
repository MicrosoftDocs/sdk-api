---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DhcpAuditLogSetParams function


## -description


The <b>DhcpAuditLogSetParams</b> function sets the parameters for audit log generation on a DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Specifies a set of bit flags for filtering the audit log. Currently, this parameter is reserved and should be set to 0.


### -param AuditLogDir [in]

Unicode string that contains the specific directory and file name  where the audit log will be stored. This string should contain the absolute path within the file system; for example, "C:\logs\dhcp\20031020.log".


### -param DiskCheckInterval [in]

Specifies the disk check interval for attempting to write the audit log to the specified file as the number of logged DHCP server events that should occur between checks. The default is 50 DHCP server events between checks.


### -param MaxLogFilesSize [in]

Specifies the maximum log file size, in bytes.


### -param MinSpaceOnDisk [in]

Specifies the minimum required disk space, in bytes, for  audit log storage.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

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
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3d0f8f06-d6a6-40b0-a3e8-0e155caee883">DhcpAuditLogGetParams</a>
 

 

