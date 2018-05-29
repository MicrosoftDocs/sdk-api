---
UID: NF:netioapi.GetMulticastIpAddressEntry
title: GetMulticastIpAddressEntry function
author: windows-sdk-content
description: Retrieves information for an existing multicast IP address entry on the local computer.
old-location: iphlp\getmulticastipaddressentry.htm
old-project: IpHlp
ms.assetid: dc6401b6-7692-44a5-b2f0-4e729b996765
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetMulticastIpAddressEntry, GetMulticastIpAddressEntry function [IP Helper], iphlp.getmulticastipaddressentry, netioapi/GetMulticastIpAddressEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetMulticastIpAddressEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetMulticastIpAddressEntry function


## -description


The 
<b>GetMulticastIpAddressEntry</b> function  retrieves information for an existing multicast IP address entry on the local computer. 


## -parameters




### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> structure entry for a multicast IP address entry. On successful return, this structure will be updated with the properties for an existing multicast IP address.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is not set to a valid multicast IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_MULTICASTIPADDRESS_ROW</b> pointed to by the <i>Row</i> parameter are unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter does not match the IP address and address family specified in the <b>Address</b> member in the <b>MIB_MULTICASTIPADDRESS_ROW</b>  structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address is specified in the <b>Address</b> member <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address is specified in the <b>Address</b> member. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetMulticastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>GetMulticastIpAddressEntry</b> function is used to retrieve an existing <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> structure entry.  

On input, the <b>Address</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid multicast IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_MULTICASTIPADDRESS_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value is set for the  <b>InterfaceLuid</b> member (the value of this member is set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output when the call is successful, <b>GetMulticastIpAddressEntry</b> retrieves the other properties for the multicast IP address and fills out the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552570">GetMulticastIpAddressTable</a> function can be called to enumerate the multicast IP address entries on a local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552570">GetMulticastIpAddressTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559277">MIB_MULTICASTIPADDRESS_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559281">MIB_MULTICASTIPADDRESS_TABLE</a>
 

 

