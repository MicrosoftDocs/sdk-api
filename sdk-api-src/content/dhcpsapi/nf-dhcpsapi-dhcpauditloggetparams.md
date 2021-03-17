---
UID: NF:dhcpsapi.DhcpAuditLogGetParams
title: DhcpAuditLogGetParams function (dhcpsapi.h)
description: Returns the audit log configuration settings from the DHCP server.
helpviewer_keywords: ["DhcpAuditLogGetParams","DhcpAuditLogGetParams function [DHCP]","dhcp.dhcpauditloggetparams","dhcpsapi/DhcpAuditLogGetParams"]
old-location: dhcp\dhcpauditloggetparams.htm
tech.root: DHCP
ms.assetid: 3d0f8f06-d6a6-40b0-a3e8-0e155caee883
ms.date: 12/05/2018
ms.keywords: DhcpAuditLogGetParams, DhcpAuditLogGetParams function [DHCP], dhcp.dhcpauditloggetparams, dhcpsapi/DhcpAuditLogGetParams
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DhcpAuditLogGetParams
 - dhcpsapi/DhcpAuditLogGetParams
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
 - DhcpAuditLogGetParams
---

# DhcpAuditLogGetParams function


## -description

The <b>DhcpAuditLogGetParams</b> function returns the audit log configuration settings from the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a set of bit flags for filtering the audit log. Currently, this parameter is reserved and should be set to 0.

### -param AuditLogDir [out]

Unicode string that contains the directory   where the audit log is stored as an absolute path within the file system.

### -param DiskCheckInterval [out]

Specifies the disk check interval for attempting to write the audit log to the specified file as the number of logged DHCP server events that should occur between checks. The default is 50 DHCP server events between checks.

### -param MaxLogFilesSize [out]

Specifies the maximum log file size, in bytes.

### -param MinSpaceOnDisk [out]

Specifies the minimum required disk space, in bytes,  for  audit log storage.

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

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpauditlogsetparams">DhcpAuditLogSetParams</a>