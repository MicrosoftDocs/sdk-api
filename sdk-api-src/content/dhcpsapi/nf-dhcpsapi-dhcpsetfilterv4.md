---
UID: NF:dhcpsapi.DhcpSetFilterV4
title: DhcpSetFilterV4 function
author: windows-driver-content
description: Enables or disables the allow and deny lists on a DHCP server.
old-location: dhcp\dhcpsetfilterv4.htm
old-project: DHCP
ms.assetid: 4a67ad11-1f24-4ab6-b5f7-e51c97562037
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpSetFilterV4, DhcpSetFilterV4 function [DHCP], dhcp.dhcpsetfilterv4, dhcpsapi/DhcpSetFilterV4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpSetFilterV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetFilterV4 function


## -description


The <b>DhcpSetFilterV4</b> function enables or disables the allow and deny lists on a DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param GlobalFilterInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/babf9cdb-bd43-41ea-9cb4-209ff129b0f2">DHCP_FILTER_GLOBAL_INFO</a> structure that contains information used to enable or disable allow and deny lists.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>
 




## -remarks



When filtering is enabled, the DHCP server allows the DHCP clients associated with link-layer addresses in the 'allow' list to be provided with leases, and blocks DHCP clients associated with addresses in the 'deny' list.




## -see-also




<a href="https://msdn.microsoft.com/babf9cdb-bd43-41ea-9cb4-209ff129b0f2">DHCP_FILTER_GLOBAL_INFO</a>
 

 

