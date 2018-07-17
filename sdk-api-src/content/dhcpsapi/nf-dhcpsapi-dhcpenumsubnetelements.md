---
UID: NF:dhcpsapi.DhcpEnumSubnetElements
title: DhcpEnumSubnetElements function
author: windows-sdk-content
description: Returns an enumerated list of elements for a specific DHCP subnet.
old-location: dhcp\dhcpenumsubnetelements.htm
old-project: DHCP
ms.assetid: 1e2f1476-2a73-4298-80f7-c57efdc10fd2
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DhcpEnumSubnetElements, DhcpEnumSubnetElements function [DHCP], dhcp.dhcpenumsubnetelements, dhcpsapi/DhcpEnumSubnetElements
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DhcpEnumSubnetElements
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpEnumSubnetElements function


## -description



      The <b>DhcpEnumSubnetElements</b> function returns an enumerated list of elements for a specific DHCP subnet.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IPv4 address of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the address of the IPv4 subnet whose elements will be enumerated.


### -param EnumElementType [in]


<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value that indicates the type of subnet element to enumerate.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet elements  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

The presence of additional enumerable data is indicated when this function returns ERROR_MORE_DATA. If no additional enumerable data is available on the DHCPv4 server, ERROR_NO_MORE_ITEMS is returned.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet elements to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

To retrieve all the subnet client elements for the default user and vendor class at the specified level, set this parameter to 0xFFFFFFFF.


### -param EnumElementInfo [out]

Pointer to a pointer to a  <a href="https://msdn.microsoft.com/50fbcae7-ea0c-4b46-a042-d463ab496e12">DHCP_SUBNET_ELEMENT_INFO_ARRAY</a> structure containing an enumerated list of all elements available for the specified subnet. If no elements are available for enumeration, this value will be null.


### -param ElementsRead [out]

Pointer to a DWORD value that specifies the number of subnet elements returned in <i>EnumElementInfo</i>.


### -param ElementsTotal [out]

Pointer to a DWORD value that specifies the total number of as-yet unenumerated elements remaining on the server for the specified subnet.


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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist on the DHCP server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/50fbcae7-ea0c-4b46-a042-d463ab496e12">
		  DHCP_SUBNET_ELEMENT_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">
		  DHCP_SUBNET_ELEMENT_TYPE</a>



<a href="https://msdn.microsoft.com/561a7aac-eed9-4a80-a4a4-f3a7727ae92a">DhcpEnumSubnetElementsV4</a>



<a href="https://msdn.microsoft.com/d6fd543c-5036-469e-9e48-02573c7dcb9f">DhcpEnumSubnetElementsV5</a>
 

 

