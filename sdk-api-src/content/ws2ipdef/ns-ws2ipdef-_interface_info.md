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

# _INTERFACE_INFO structure


## -description



			The 
<b>INTERFACE_INFO</b> structure is used in conjunction with the <b>SIO_GET_INTERFACE_LIST</b> ioctl command to obtain information about an interface IP address.


## -struct-fields




### -field iiFlags

A bitmask describing the status of the interface. The following flags are possible.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IFF_UP"></a><a id="iff_up"></a><dl>
<dt><b>IFF_UP</b></dt>
</dl>
</td>
<td width="60%">
The interface is running.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_BROADCAST"></a><a id="iff_broadcast"></a><dl>
<dt><b>IFF_BROADCAST</b></dt>
</dl>
</td>
<td width="60%">
The broadcast feature is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_LOOPBACK"></a><a id="iff_loopback"></a><dl>
<dt><b>IFF_LOOPBACK</b></dt>
</dl>
</td>
<td width="60%">
The loopback interface is running.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_POINTTOPOINT"></a><a id="iff_pointtopoint"></a><dl>
<dt><b>IFF_POINTTOPOINT</b></dt>
</dl>
</td>
<td width="60%">
The interface is using point-to-point link.

</td>
</tr>
<tr>
<td width="40%"><a id="IFF_MULTICAST"></a><a id="iff_multicast"></a><dl>
<dt><b>IFF_MULTICAST</b></dt>
</dl>
</td>
<td width="60%">
The multicast feature is supported.

</td>
</tr>
</table>
 


### -field iiAddress

Address of an interface.


### -field iiBroadcastAddress

Broadcast address of the interface or the address of the other side for point-to-point links.


### -field iiNetmask

Netmask used by the interface.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>INTERFACE_INFO</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/6a63c2c9-4e09-4a62-b39f-3ccb26287da8">Winsock IOCTLs</a>
 

 

