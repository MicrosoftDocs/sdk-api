---
UID: NF:dhcpsapi.DhcpRemoveSubnetElementV6
title: DhcpRemoveSubnetElementV6 function
author: windows-sdk-content
description: The DhcpRemoveSubnetElementV6 function removes an element from a subnet defined on the DHCP server.
old-location: dhcp\dhcpremovesubnetelementv6.htm
old-project: DHCP
ms.assetid: 02efbce8-ac9c-4e8e-96d0-cdb556204b3d
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DhcpRemoveSubnetElementV6, DhcpRemoveSubnetElementV6 function [DHCP], dhcp.dhcpremovesubnetelementv6, dhcpsapi/DhcpRemoveSubnetElementV6
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
 - DhcpRemoveSubnetElementV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpRemoveSubnetElementV6 function


## -description


The <b>DhcpRemoveSubnetElementV6</b> function removes an element from a subnet defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS value that specifies the IP address of the subnet gateway and uniquely identifies it.


### -param RemoveElementInfo [in]

DHCP_SUBNET_ELEMENT_DATA_V6 structure that contains information used to find the element that will be removed from subnet specified in <i>SubnetAddress</i>.


### -param ForceFlag [in]


<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a> enumeration value that indicates whether or not the clients affected by the removal of the subnet element should also be deleted.


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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified scope element does not exist.

</td>
</tr>
</table>
 



