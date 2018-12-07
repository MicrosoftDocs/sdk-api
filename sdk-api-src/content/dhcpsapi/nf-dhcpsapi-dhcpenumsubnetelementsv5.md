---
UID: NF:dhcpsapi.DhcpEnumSubnetElementsV5
title: DhcpEnumSubnetElementsV5 function
author: windows-sdk-content
description: The DhcpEnumSubnetElementsV5 function returns an enumerated list of elements for a specific DHCP subnet.
old-location: dhcp\dhcpenumsubnetelementsv5.htm
tech.root: DHCP
ms.assetid: d6fd543c-5036-469e-9e48-02573c7dcb9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpEnumSubnetElementsV5, DhcpEnumSubnetElementsV5 function [DHCP], dhcp.dhcpenumsubnetelementsv5, dhcpsapi/DhcpEnumSubnetElementsV5
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpEnumSubnetElementsV5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpEnumSubnetElementsV5 function


## -description


The <b>DhcpEnumSubnetElementsV5</b> function returns an enumerated list of elements for a specific DHCP subnet.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the address of the IP subnet whose elements will be enumerated.


### -param EnumElementType [in]


<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">DHCP_SUBNET_ELEMENT_TYPE</a> enumeration value that indicates the type of subnet element to enumerate.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet elements  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

The presence of additional enumerable data is indicated when this function returns ERROR_MORE_DATA. If no additional enumerable data is available on the DHCPv4 server, ERROR_NO_MORE_ITEMS is returned.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet elements to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

To retrieve all the subnet client elements for the default user and vendor class at the specified level, set this parameter to 0xFFFFFFFF.


### -param EnumElementInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/427683d5-e285-49b7-a68b-3c75b8b8ce23">DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5</a> structure containing an enumerated list of all elements available for the specified subnet. If no elements are available for enumeration, this value will be null.


### -param ElementsRead [out]

Pointer to a DWORD value that specifies the number of subnet elements returned in <i>EnumElementInfo</i>.


### -param ElementsTotal [out]

Pointer to a DWORD value that specifies the total number of elements for the specified subnet.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>. Common errors include the following:

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
This error can be returned when this function is called with <i>EnumElementType</i> set to <b>DhcpIpRangesDhcpOnly</b> or <b>DhcpIpRangesDhcpBootp</b>.

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
</table>
 




## -remarks



When no longer needed, the resources consumed for the  enumerated data, and all pointers contained within, should be released with <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/427683d5-e285-49b7-a68b-3c75b8b8ce23">DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5</a>



<a href="https://msdn.microsoft.com/291be329-0588-4b67-835f-4f2b2369772a">DHCP_SUBNET_ELEMENT_TYPE</a>
 

 

