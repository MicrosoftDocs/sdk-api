---
UID: NF:netioapi.CreateIpForwardEntry2
title: CreateIpForwardEntry2 function
author: windows-sdk-content
description: Creates a new IP route entry on the local computer.
old-location: iphlp\createipforwardentry2.htm
tech.root: IpHlp
ms.assetid: d2d065d3-daad-4167-8b87-4229199ee76a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateIpForwardEntry2, CreateIpForwardEntry2 function [IP Helper], iphlp.createipforwardentry2, netioapi/CreateIpForwardEntry2
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
 - CreateIpForwardEntry2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateIpForwardEntry2 function


## -description


The 
<b>CreateIpForwardEntry2</b> function  creates a new IP route entry on the local computer. 


## -parameters




### -param Row [in]

A pointer to a 
<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. 


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter was not specified, the <b>NextHop</b> member of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Row</i> parameter was not specified, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Row</i> parameter were unspecified. This error is also returned if the <b>PreferredLifetime</b> member specified in the <b>MIB_IPFORWARD_ROW2</b> is greater than the <b>ValidLifetime</b> member or if the <b>SitePrefixLength</b> in the <b>MIB_IPFORWARD_ROW2</b> is greater than the prefix length specified in the <b>DestinationPrefix</b>. 

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
The request is not supported. This error is returned if the interface specified does not support routes. This error is also returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the address family in the <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b>  was specified for the address family in the <b>DestinationPrefix</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_ALREADY_EXISTS </b></dt>
</dl>
</td>
<td width="60%">
The object already exists. This error is returned if the  <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter is a duplicate of an existing IP route entry on the interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <b>MIB_IPFORWARD_ROW2</b>.  

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



The <b>CreateIpForwardEntry2</b> function is defined on Windows Vista and later. 

The <b>CreateIpForwardEntry2</b> function is used to add a new neighbor IP address entry on a local computer. The <a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a> function should be used to initialize the members of a
    <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry with default values.  An application can then change the
    members in the <b>MIB_IPFORWARD_ROW2</b> entry it wishes to modify, and then call the <b>CreateIpForwardEntry2</b> function.

The <b>DestinationPrefix</b> member in the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid IPv4 or IPv6 address prefix. The <b>NextHop</b> member in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to by the <i>Row</i> parameter must be initialized to a valid IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to the <i>Row</i> parameter must be initialized to the interface: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface on which to add the IP route entry. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

The route metric offset specified in the <b>Metric</b> member of the  <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Row</i> parameter represents only part of the complete route metric. The complete metric is a combination of this route metric  offset added to the interface metric specified in the <b>Metric</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  An application can retrieve the interface metric by calling the <a href="https://msdn.microsoft.com/604e33fd-ab12-4861-a083-544045f46ef4">GetIpInterfaceEntry</a> function.

The <b>Age</b> and <b>Origin</b> members of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> are ignored when the  <b>CreateIpForwardEntry2</b> function is called. These members are set by the network stack and cannot be set using the <b>CreateIpForwardEntry2</b> function.

The <b>CreateIpForwardEntry2</b> function will fail if the <b>DestinationPrefix</b> and <b>NextHop</b> members of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter are a duplicate of an existing IP route entry on the interface specified in the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members. 

The <b>CreateIpForwardEntry2</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateIpForwardEntry2</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/53d5009a-d205-40ce-88e5-fe37e72b5a50">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/604e33fd-ab12-4861-a083-544045f46ef4">GetIpInterfaceEntry</a>



<a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>
 

 

