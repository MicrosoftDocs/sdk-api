---
UID: NF:dhcpsapi.DhcpServerRestoreDatabase
title: DhcpServerRestoreDatabase function (dhcpsapi.h)
description: Restores the settings, configuration, and records for a client lease database from a specific backup location (path).
helpviewer_keywords: ["DhcpServerRestoreDatabase","DhcpServerRestoreDatabase function [DHCP]","dhcp.dhcpserverrestoredatabase","dhcpsapi/DhcpServerRestoreDatabase"]
old-location: dhcp\dhcpserverrestoredatabase.htm
tech.root: DHCP
ms.assetid: b7003fcc-bff1-449d-8849-c02932880114
ms.date: 12/05/2018
ms.keywords: DhcpServerRestoreDatabase, DhcpServerRestoreDatabase function [DHCP], dhcp.dhcpserverrestoredatabase, dhcpsapi/DhcpServerRestoreDatabase
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
 - DhcpServerRestoreDatabase
 - dhcpsapi/DhcpServerRestoreDatabase
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
 - DhcpServerRestoreDatabase
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

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpscandatabase">DhcpScanDatabase</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpserverbackupdatabase">DhcpServerBackupDatabase</a>