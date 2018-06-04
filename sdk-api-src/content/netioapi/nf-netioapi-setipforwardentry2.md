---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetIpForwardEntry2 function


## -description


The 
<b>SetIpForwardEntry2</b> function  sets the properties of an IP route entry on the local computer.


## -parameters




### -param Route [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. The <b>DestinationPrefix</b> member of the <b>MIB_IPFORWARD_ROW2</b> must be set to a valid IP destination prefix, the <b>NextHop</b> member of the <b>MIB_IPFORWARD_ROW2</b> must be set to a valid IP address family and IP address,   and the <b>InterfaceLuid</b> or the  <b>InterfaceIndex</b> member of the <b>MIB_IPFORWARD_ROW2</b> must be specified. 


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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Route</i> parameter, the <b>DestinationPrefix</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Route</i> parameter was not specified, the <b>NextHop</b> member of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Route</i> parameter was not specified, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPFORWARD_ROW2</b> pointed to by the <i>Route</i> parameter were unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Route</i> parameter could not be found.  

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



The <b>SetIpForwardEntry2</b> function is defined on Windows Vista and later. 

The <b>SetIpForwardEntry2</b> function is used to set the properties for an existing IP route entry on a local computer. 

The <b>DestinationPrefix</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Route</i> parameter must be initialized to a valid IP address prefix and family. The <b>NextHop</b> member in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to by the <i>Route</i> parameter must be initialized to a valid IP address and family. In addition, at least one of the following members in the <b>MIB_IPFORWARD_ROW2</b> structure pointed to the <i>Route</i> parameter must be initialized to the interface: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface on which to add the unicast IP address. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

The route metric offset specified in the <b>Metric</b> member of the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Route</i> parameter represents only part of the complete route metric. The complete metric is a combination of this route metric  offset added to the interface metric specified in the <b>Metric</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559254">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  An application can retrieve the interface metric by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552540">GetIpInterfaceEntry</a> function.

The <b>Age</b> and <b>Origin</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> structure pointed to by the <i>Row</i> are ignored when the  <b>SetIpForwardEntry2</b> function is called. These members are set by the network stack and cannot be changed using the <b>SetIpForwardEntry2</b> function.

The <b>SetIpForwardEntry2</b> function will fail if the  <b>DestinationPrefix</b> and <b>NextHop</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a> pointed to by the <i>Route</i> parameter do not match an IP route entry on the interface specified. 

The <b>SetIpForwardEntry2</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIpForwardEntry2</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>SetIpForwardEntry2</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546365">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552511">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552535">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552536">GetIpForwardTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552540">GetIpInterfaceEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554882">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559245">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559252">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559254">MIB_IPINTERFACE_ROW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568806">NotifyRouteChange2</a>
 

 

