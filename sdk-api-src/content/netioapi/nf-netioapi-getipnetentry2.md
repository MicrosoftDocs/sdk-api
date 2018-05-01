---
UID: NF:netioapi.GetIpNetEntry2
title: GetIpNetEntry2 function
author: windows-driver-content
description: Retrieves information for a neighbor IP address entry on the local computer.
old-location: iphlp\getipnetentry2.htm
old-project: IpHlp
ms.assetid: c77e01da-2d5a-4c74-b581-62fa6ee52c9e
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetIpNetEntry2, GetIpNetEntry2 function [IP Helper], iphlp.getipnetentry2, netioapi/GetIpNetEntry2
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	GetIpNetEntry2
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# GetIpNetEntry2 function


## -description


The 
<b>GetIpNetEntry2</b> function  retrieves information for a neighbor IP address entry on the local computer. 


## -parameters




### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure entry for a neighbor IP address entry. On successful return, this structure will be updated with the properties for neighbor IP address.


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
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter was not set to a valid neighbor IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPNET_ROW2</b> pointed to by the <i>Row</i> parameter were unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure pointed to by the <i>Row</i> parameter does not match the neighbor IP address and address family specified in the <b>Address</b> member in the <b>MIB_IPNET_ROW2</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <b>Address</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address was specified in the <b>Address</b> member of the <b>MIB_IPNET_ROW2</b> structure.

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



The <b>GetIpNetEntry2</b> function is defined on Windows Vista and later. 

The <b>GetIpNetEntry2</b> function is used to retrieve a <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure entry.  

On input, the <b>Address</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid neighbor IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_IPNET_ROW2</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output when the call is successful, <b>GetIpNetEntry2</b> retrieves the other properties for the neighbor IP address and fills out the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure pointed to by the <i>Row</i> parameter. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a> function can be called to enumerate the neighbor IP address entries on a local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546217">CreateIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546368">DeleteIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550029">FlushIpNetTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559267">MIB_IPNET_TABLE2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570775">SetIpNetEntry2</a>
 

 

