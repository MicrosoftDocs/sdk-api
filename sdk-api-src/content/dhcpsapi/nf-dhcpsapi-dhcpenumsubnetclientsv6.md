---
UID: NF:dhcpsapi.DhcpEnumSubnetClientsV6
title: DhcpEnumSubnetClientsV6 function
author: windows-sdk-content
description: The DhcpEnumSubnetClientsV6 function returns an enumerated list of clients with served IP addresses in the specified subnet.
old-location: dhcp\dhcpenumsubnetclientsv6.htm
old-project: dhcp
ms.assetid: 501a9cd4-56ff-4b56-9d08-83cb29932ef7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpEnumSubnetClientsV6, DhcpEnumSubnetClientsV6 function [DHCP], dhcp.dhcpenumsubnetclientsv6, dhcpsapi/DhcpEnumSubnetClientsV6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpEnumSubnetClientsV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpEnumSubnetClientsV6 function


## -description


The <b>DhcpEnumSubnetClientsV6</b> function returns an enumerated list of clients with served IP addresses in the specified subnet.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> value containing the IP address of the subnet gateway.


### -param ResumeHandle [in, out]

Pointer to a DHCP_RESUME_IPV6_HANDLE value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet client information structures  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet client information structures to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.


### -param ClientInfo [out]

Pointer to a DHCP_CLIENT_INFO_ARRAY_V6 structure containing information on the clients served under this specific subnet. If no clients are available, this field will be null.


### -param ClientsRead [out]

Pointer to a DWORD value that specifies the number of clients returned in <i>ClientInfo</i>.


### -param ClientsTotal [out]

Pointer to a DWORD value that specifies the total number of clients for the specified subnet stored on the DHCP server.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more items to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More data is available to enumerate.

</td>
</tr>
</table>
 



