---
UID: NF:dhcpsapi.DhcpServerBackupDatabase
title: DhcpServerBackupDatabase function (dhcpsapi.h)
description: Backs up the DHCP server database configuration, settings, and DHCP client lease record to a specified file location.
helpviewer_keywords: ["DhcpServerBackupDatabase","DhcpServerBackupDatabase function [DHCP]","dhcp.dhcpserverbackupdatabase","dhcpsapi/DhcpServerBackupDatabase"]
old-location: dhcp\dhcpserverbackupdatabase.htm
tech.root: DHCP
ms.assetid: 90e37a33-6d58-4bfc-99e7-e1c244f927ed
ms.date: 12/05/2018
ms.keywords: DhcpServerBackupDatabase, DhcpServerBackupDatabase function [DHCP], dhcp.dhcpserverbackupdatabase, dhcpsapi/DhcpServerBackupDatabase
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpServerBackupDatabase
 - dhcpsapi/DhcpServerBackupDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpServerBackupDatabase
---

# DhcpServerBackupDatabase function


## -description

The <b>DhcpServerBackupDatabase</b> function backs up the DHCP server database configuration, settings, and DHCP client lease record to a specified file location.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Path [in]

Unicode string that specifies the absolute path to the file where the DHCP server database will be backed up.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserverrestoredatabase">DhcpServerRestoreDatabase</a>