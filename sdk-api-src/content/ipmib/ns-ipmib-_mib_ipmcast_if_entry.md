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

# _MIB_IPMCAST_IF_ENTRY structure


## -description


The 
<b>MIB_IPMCAST_IF_ENTRY</b> structure stores information about an IP multicast interface.


## -struct-fields




### -field dwIfIndex

The index of this interface.


### -field dwTtl

The time-to-live value for this interface.


### -field dwProtocol

The multicast routing protocol that owns this interface.


### -field dwRateLimit

The rate limit of this interface.


### -field ulInMcastOctets

The number of octets of multicast data received through this interface.


### -field ulOutMcastOctets

The number of octets of multicast data sent through this interface.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/6ea374e3-cb09-44e5-b80a-b68447589191">MIB_IPMCAST_IF_TABLE</a>
 

 

