---
UID: NF:dhcpsapi.DhcpServerRestoreDatabase
title: DhcpServerRestoreDatabase function
author: windows-driver-content
description: Restores the settings, configuration, and records for a client lease database from a specific backup location (path).
old-location: dhcp\dhcpserverrestoredatabase.htm
old-project: DHCP
ms.assetid: b7003fcc-bff1-449d-8849-c02932880114
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DhcpServerRestoreDatabase, DhcpServerRestoreDatabase function [DHCP], dhcp.dhcpserverrestoredatabase, dhcpsapi/DhcpServerRestoreDatabase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpServerRestoreDatabase
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpServerRestoreDatabase function


## -description


The <b>DhcpServerRestoreDatabase</b> function restores the settings, configuration, and records for a client lease database from a specific backup location (path).


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Path [in]

Unicode string that specifies the full absolute path and filename to the backup file from which the registry configuration file and client lease database will be restored. Note that this operation will overwrite any database currently held in memory.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6324c197-7237-449f-ae23-4f04b1b7498e">DhcpScanDatabase</a>



<a href="https://msdn.microsoft.com/90e37a33-6d58-4bfc-99e7-e1c244f927ed">DhcpServerBackupDatabase</a>
 

 

