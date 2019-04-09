---
UID: NF:netioapi.GetIpForwardEntry2
title: GetIpForwardEntry2 function (netioapi.h)
author: windows-sdk-content
description: Retrieves information for an IP route entry on the local computer.
old-location: iphlp\getipforwardentry2.htm
tech.root: IpHlp
ms.assetid: 53d5009a-d205-40ce-88e5-fe37e72b5a50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIpForwardEntry2, GetIpForwardEntry2 function [IP Helper], iphlp.getipforwardentry2, netioapi/GetIpForwardEntry2
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
 - GetIpForwardEntry2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIpForwardEntry2 function


## -description


The 
<b>GetIpForwardEntry2</b> function  retrieves information for an IP route entry on the local computer. 


## -parameters




### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. On successful return, this structure will be updated with the properties for the IP route entry.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter was not specified, the <b>NextHop</b> member of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Row</i> parameter was not specified, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Row</i> parameter were unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> parameter does not match the IP address prefix and address family specified in the <b>DestinationPrefix</b>  member in the <b>MIB_IPFORWARD_ROW2</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the address family in the <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b>  was specified for the address family in the <b>DestinationPrefix</b> member.

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



The <b>GetIpForwardEntry2</b> function is defined on Windows Vista and later. 

The <b>GetIpForwardEntry2</b> function is used to retrieve a <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure entry.  

On input, the <b>DestinationPrefix</b> member in the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid IPv4 or IPv6 address prefix and family. On input, the <b>NextHop</b> member in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to by the <i>Row</i> parameter must be initialized to a valid IPv4 or IPv6 address and family. In addition, at least one of the following members in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output when the call is successful, <b>GetIpForwardEntry2</b> retrieves the other properties for the IP route entry and fills out the <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> parameter. 

The route metric offset specified in the <b>Metric</b> member of the  <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Row</i> parameter represents only part of the complete route metric. The complete metric is a combination of this route metric  added to the interface metric specified in the <b>Metric</b> member of the <a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  An application can retrieve the interface metric by calling the <a href="https://msdn.microsoft.com/604e33fd-ab12-4861-a083-544045f46ef4">GetIpInterfaceEntry</a> function.

The <a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a> function can be called to enumerate the IP route entries on a local computer.




## -see-also




<a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/14412ef1-d970-419d-abfa-389f6ceb638d">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/604e33fd-ab12-4861-a083-544045f46ef4">GetIpInterfaceEntry</a>



<a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>
 

 

