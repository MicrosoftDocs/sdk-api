---
UID: NF:netioapi.CreateIpNetEntry2
title: CreateIpNetEntry2 function (netioapi.h)
author: windows-sdk-content
description: Creates a new neighbor IP address entry on the local computer.
old-location: iphlp\createipnetentry2.htm
tech.root: IpHlp
ms.assetid: ca92b9f8-ec3c-4889-b649-f606c3920f92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateIpNetEntry2, CreateIpNetEntry2 function [IP Helper], iphlp.createipnetentry2, netioapi/CreateIpNetEntry2
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CreateIpNetEntry2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateIpNetEntry2 function


## -description


The 
<b>CreateIpNetEntry2</b> function  creates a new neighbor IP address entry on the local computer. 


## -parameters




### -param Row [in]

A pointer to a 
<a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> structure entry for a neighbor IP address entry. 


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter was not set to a valid unicast, anycast, or multicast IPv4 or IPv6 address, the <b>PhysicalAddress</b> and <b>PhysicalAddressLength</b> members of the <b>MIB_IPNET_ROW2</b> pointed to by the <i>Row</i> parameter were not set to a valid physical address,  or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPNET_ROW2</b> pointed to by the <i>Row</i> parameter were unspecified. This error is also returned if a loopback address was passed in the <b>Address</b> member. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <b>Address</b> member of the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address was specified in the <b>Address</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_ALREADY_EXISTS </b></dt>
</dl>
</td>
<td width="60%">
The object already exists. This error is returned if the  <b>Address</b> member of the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter is a duplicate of an existing neighbor IP address on the interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <b>MIB_IPNET_ROW2</b>.  

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



The <b>CreateIpNetEntry2</b> function is defined on Windows Vista and later. 

The <b>CreateIpNetEntry2</b> function is used to add a new neighbor IP address entry on a local computer. 

The <b>Address</b> member in the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid unicast, anycast, or multicast IPv4 or IPv6 address and family. The  <b>PhysicalAddress</b> and <b>PhysicalAddressLength</b> members in the <b>MIB_IPNET_ROW2</b> structure pointed to by the <i>Row</i> parameter must be initialized to a valid physical address. In addition, at least one of the following members in the <b>MIB_IPNET_ROW2</b> structure pointed to the <i>Row</i> parameter must be initialized to the interface: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface on which to add the unicast IP address. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

The <b>CreateIpNetEntry2</b> function will fail if the IP address passed in the <b>Address</b> member of the <a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a> pointed to by the <i>Row</i> parameter is a duplicate of an existing neighbor IP address on the interface. 

The <b>CreateIpNetEntry2</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateIpNetEntry2</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/85bace04-6c95-4cf2-a212-764de292aed6">DeleteIpNetEntry2</a>



<a href="https://msdn.microsoft.com/6ebfca41-acc3-450c-a3c5-881b8c3fca5e">FlushIpNetTable2</a>



<a href="https://msdn.microsoft.com/c77e01da-2d5a-4c74-b581-62fa6ee52c9e">GetIpNetEntry2</a>



<a href="https://msdn.microsoft.com/6c45d735-9a07-41ca-8d8a-919f32c98a3c">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/164dbd93-4464-40f9-989a-17597102b1d8">MIB_IPNET_ROW2</a>



<a href="https://msdn.microsoft.com/39b87d81-69ce-4f9b-8af6-5e0c5051657c">MIB_IPNET_TABLE2</a>



<a href="https://msdn.microsoft.com/37f9dc58-362d-413e-a593-4dda52fb7d8b">ResolveIpNetEntry2</a>



<a href="https://msdn.microsoft.com/4f423700-f721-44a9-ade3-ea5b5b86e394">SetIpNetEntry2</a>
 

 

