---
UID: NF:dhcpsapi.DhcpCreateClass
title: DhcpCreateClass function
author: windows-driver-content
description: Creates a custom option class.
old-location: dhcp\dhcpcreateclass.htm
old-project: DHCP
ms.assetid: ae30baba-a2cd-4662-a62a-58b59d119dc4
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DhcpCreateClass, DhcpCreateClass function [DHCP], dhcp.dhcpcreateclass, dhcpsapi/DhcpCreateClass
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
-	DhcpCreateClass
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpCreateClass function


## -description


The <b>DhcpCreateClass</b> function creates a custom option class.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ReservedMustBeZero [in]

Reserved. This field must be set to zero.


### -param ClassInfo [in]


<a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a> structure that contains the specific option class data.


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
<dt><b>ERROR_DHCP_CLASS_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified class name is already defined on the DHCP server, or the class information is already in use..

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">
		  DHCP_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/45659805-d0d0-4b84-ac98-4a0f53133b0c">DhcpDeleteClass</a>



<a href="https://msdn.microsoft.com/93f37424-1a81-477e-85da-359885e94349">DhcpEnumClasses</a>
 

 

