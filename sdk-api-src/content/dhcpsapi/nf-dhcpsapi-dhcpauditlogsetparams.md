---
UID: NF:dhcpsapi.DhcpAuditLogSetParams
title: DhcpAuditLogSetParams function (dhcpsapi.h)
description: Sets the parameters for audit log generation on a DHCP server.
helpviewer_keywords: ["DhcpAuditLogSetParams","DhcpAuditLogSetParams function [DHCP]","dhcp.dhcpauditlogsetparams","dhcpsapi/DhcpAuditLogSetParams"]
old-location: dhcp\dhcpauditlogsetparams.htm
tech.root: DHCP
ms.assetid: ea7fc321-3e7c-4d1f-9a39-6a25d0d1c5b2
ms.date: 12/05/2018
ms.keywords: DhcpAuditLogSetParams, DhcpAuditLogSetParams function [DHCP], dhcp.dhcpauditlogsetparams, dhcpsapi/DhcpAuditLogSetParams
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
 - DhcpAuditLogSetParams
 - dhcpsapi/DhcpAuditLogSetParams
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
 - DhcpAuditLogSetParams
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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpauditloggetparams">DhcpAuditLogGetParams</a>