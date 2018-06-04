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

# _MIB_IPMCAST_MFE structure


## -description


The 
<b>MIB_IPMCAST_MFE</b> structure stores the information for an Internet Protocol (IP) Multicast Forwarding Entry (MFE).


## -struct-fields




### -field dwGroup

Type: <b>DWORD</b>

The range of IPv4 multicast groups for this MFE. A value of zero indicates a wildcard group.


### -field dwSource

Type: <b>DWORD</b>

The range of IPv4 source addresses for this MFE. A value of zero indicates a wildcard source.


### -field dwSrcMask

Type: <b>DWORD</b>

The IPv4 subnet mask that corresponds to <b>dwSourceAddr</b>. The <b>dwSourceAddr</b> and <b>dwSourceMask</b> members are used together to define a range of sources.


### -field dwUpStrmNgbr

Type: <b>DWORD</b>

The upstream neighbor that is related to this MFE.


### -field dwInIfIndex

Type: <b>DWORD</b>

The index of the interface to which this MFE is related.


### -field dwInIfProtocol

Type: <b>DWORD</b>

The routing protocol that owns the incoming interface to which this MFE is related.


### -field dwRouteProtocol

Type: <b>DWORD</b>

The client that created the route.


### -field dwRouteNetwork

Type: <b>DWORD</b>

The IPv4 address associated with the route referred to by <b>dwRouteProtocol</b>.


### -field dwRouteMask

Type: <b>DWORD</b>

The IPv4 mask associated with the route referred to by <b>dwRouteProtocol</b>.


### -field ulUpTime

Type: <b>ULONG</b>

The time, in seconds, this MFE has been valid. This value starts from zero and is incremented until it reaches the <b>ulTimeOut</b> value, at which time the MFE is deleted.


### -field ulExpiryTime

Type: <b>ULONG</b>

The time, in seconds, that remains before the MFE expires and is deleted. This value starts from <b>ulTimeOut</b> and is decremented until it reaches zero, at which time the MFE is deleted.


### -field ulTimeOut

Type: <b>ULONG</b>

The total length of time, in seconds, that this MFE should remain valid. After the time-out value is exceeded, the MFE is deleted. This value is static.


### -field ulNumOutIf

Type: <b>ULONG</b>

The number of outgoing interfaces that are associated with this MFE.


### -field fFlags

Type: <b>DWORD</b>

Reserved. This member should be <b>NULL</b>.


### -field dwReserved

Type: <b>DWORD</b>

Reserved. This member should be <b>NULL</b>.


### -field rgmioOutInfo

Type: <b>MIB_IPMCAST_OIF[ANY_SIZE]</b>

A pointer to a table of outgoing interface statistics that are implemented as an array of 
<a href="https://msdn.microsoft.com/4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40">MIB_IPMCAST_OIF</a> structures.


## -remarks



The 
<b>MIB_IPMCAST_MFE</b> structure does not have a fixed size. Use the <b>SIZEOF_MIB_MFE(X)</b> macro to determine the size of this structure. This macro is defined in the Iprtrmib.h header file.

The <b>dwRouteProtocol</b>, <b>dwRouteNetwork</b>, and <b>dwRouteMask</b> members uniquely identify the route to which this MFE is related.

The <b>MIB_IPMCAST_MFE</b> structure is used by the <a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>. The <b>MIB_IPMCAST_MFE</b> structure is retrieved using the <a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a> function. An existing <b>MIB_IPMCAST_MFE</b> structure can be modified using the <a href="https://msdn.microsoft.com/143c080a-be80-47fb-a159-e6c95aa0d7ea">MgmSetMfe</a>
			 function.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40">MIB_IPMCAST_OIF</a>



<a href="https://msdn.microsoft.com/2567e899-760d-41dd-8347-634c1a0e5764">MIB_MFE_TABLE</a>



<a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a>



<a href="https://msdn.microsoft.com/143c080a-be80-47fb-a159-e6c95aa0d7ea">MgmSetMfe</a>



<a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>
 

 

