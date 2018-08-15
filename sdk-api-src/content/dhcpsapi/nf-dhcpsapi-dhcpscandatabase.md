---
UID: NF:dhcpsapi.DhcpScanDatabase
title: DhcpScanDatabase function
author: windows-sdk-content
description: Enumerates the leased DHCPv4 client IPv4 addresses that are not synchronized between the in-memory cache and the server database.
old-location: dhcp\dhcpscandatabase.htm
old-project: dhcp
ms.assetid: 6324c197-7237-449f-ae23-4f04b1b7498e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpScanDatabase, DhcpScanDatabase function [DHCP], dhcp.dhcpscandatabase, dhcpsapi/DhcpScanDatabase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpScanDatabase
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpScanDatabase function


## -description


The <b>DhcpScanDatabase</b> function enumerates the leased DHCPv4 client IPv4 addresses that are not synchronized between the in-memory cache and the server database.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the subnet whose leases will be scanned for desynchronized client lease IP addresses.


### -param FixFlag [in]

Specifies a set of bit flags that indicate whether the in-memory cache or the client lease database should be the definitive source for fixes when synchronizing the two on the DHCPv4 server. These flags are enumerated in <a href="https://msdn.microsoft.com/825a0e64-b0c2-453e-8e00-52f84c40bef3">DHCP_SCAN_FLAG</a>.


### -param ScanList [out]


<a href="https://msdn.microsoft.com/9dc20612-1c08-4493-aab3-b524d8d88251">DHCP_SCAN_LIST</a> structure that contains the returned list of leased client IP addresses that are not in sync.


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
An error occurred while accessing the DHCPv4 server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCPv4 server.

</td>
</tr>
</table>
 




## -remarks



Each  leased DHCPv4 client IPv4 address defined on a DHCPv4 server has an entry in both an in-memory store, which serves as a cache for speeding up lease retrieval, and in the client lease database proper. <b>DhcpScanDatabase</b> enumerates either the DHCPv4 client IPv4 addresses that are present in the in-memory store and are not present in the database, or those that are present in database but not present in the in-memory store.

This process is necessary as the DHCPv4 server maintains an in-memory cache of frequently-accessed client leases used to improve performance, but it can become desynchronized relative to the server's persistent client lease database. Therefore, it is necessary to reconcile the two stores, and update either the in-memory version of a client lease IP address, or the client lease IP address stored in the database.  The <a href="https://msdn.microsoft.com/9dc20612-1c08-4493-aab3-b524d8d88251">DHCP_SCAN_LIST</a> structure returned by this operation contains the "definitive" client leases as specified by the preferred location set in the <i>FixFlag</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/9dc20612-1c08-4493-aab3-b524d8d88251">DHCP_SCAN_LIST</a>
 

 

