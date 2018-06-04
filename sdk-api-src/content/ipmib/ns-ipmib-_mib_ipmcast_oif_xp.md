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

# _MIB_IPMCAST_OIF_XP structure


## -description


The 
<b>MIB_IPMCAST_OIF</b> structure stores the information required to send an outgoing IP multicast packet.


## -struct-fields




### -field dwOutIfIndex

The index of the interface on which to send the outgoing IP multicast packet.


### -field dwNextHopAddr

The destination address for the outgoing IPv4 multicast packet.


### -field dwReserved

Reserved. This member should be zero.


### -field dwReserved1

 




#### - pvReserved

Reserved. This member should be <b>NULL</b>.


## -remarks



The <b>MIB_IPMCAST_MFE</b> structure is used by the <a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>. The <b>MIB_IPMCAST_OIF</b> structure is retrieved as a member of the <b>MIB_IPMCAST_MFE</b> structure  using the <a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a> function.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a>



<a href="https://msdn.microsoft.com/0d1a2396-883b-4ca5-b8a0-11a3d3575a61">MIB_IPMCAST_OIF_STATS</a>



<a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a>



<a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>
 

 

