---
UID: NF:dhcpsapi.DhcpV4GetFreeIPAddress
title: DhcpV4GetFreeIPAddress function
author: windows-driver-content
description: Retrieves the list of available IPv4 addresses that can be leased to clients.
old-location: dhcp\dhcpv4getfreeipaddress.htm
old-project: DHCP
ms.assetid: acce28e6-ea4a-4f27-8fb6-913f0e5aa52e
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpV4GetFreeIPAddress, DhcpV4GetFreeIPAddress function [DHCP], dhcp.dhcpv4getfreeipaddress, dhcpsapi/DhcpV4GetFreeIPAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
-	DhcpV4GetFreeIPAddress
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4GetFreeIPAddress function


## -description


The <b>DhcpV4GetFreeIPAddress</b> function retrieves the list of available IPv4 addresses that can be leased to clients.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param ScopeId [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that specifies the IPv4 subnet ID from which available addresses to lease to clients are retrieved.


### -param StartIP

TBD


### -param EndIP

TBD


### -param NumFreeAddrReq

TBD


### -param IPAddrList [out]

Pointer to a <a href="https://msdn.microsoft.com/84f42e55-8364-4119-83e4-c03699a9aa0a">DHCP_IP_ARRAY</a> structure that contains the list of available IPv4 addresses that can be leased to clients.


#### - endIP [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that specifies the scope IPv4 range's end point address from where the available addresses are retrieved. If this parameter is 0, the end address of the IPv4 subnet specified by <i>ScopeId</i> parameter is taken as the default.


#### - numFreeAddrReq [in]

Integer that specifies the number of IPv4 addresses retrieved from the specified scope in <i>IPAddrList</i>. If this parameter is 0, only one IPv4 address is returned.


#### - startIP [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that specifies the scope IPv4 range's starting point address from where the available addresses are retrieved. If this parameter is 0, the start address of the IPv4 subnet specified by <i>ScopeId</i> is the default.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_REACHED_END_OF_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP Server has reached the end of the selected range while finding the free IP address.

</td>
</tr>
</table>
 




## -remarks



<i>IPAddrList</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

The maximum number of IPv4 addresses returned is 1024. To retrieve more that 1024 IPv4 addresses, multiple calls to  <b>DhcpV4GetFreeIPAddress</b> must be made. After the initial call, each subsequent call to <b>DhcpV4GetFreeIPAddress</b> must set <i>startIP</i> to the last address in the list received in <i>IPAddrList</i> from the previous call to <b>DhcpV4GetFreeIPAddress</b>.

When the number of free IPv4 addresses available on the DHCP server is less than that requested, the list of free IPv4 addresses available are returned to the caller with error code <b>ERROR_DHCP_REACHED_END_OF_SELECTION</b>.



