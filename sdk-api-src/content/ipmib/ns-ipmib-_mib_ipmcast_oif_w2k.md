---
UID: NS:ipmib._MIB_IPMCAST_OIF_W2K
title: "_MIB_IPMCAST_OIF_W2K"
author: windows-sdk-content
description: Stores the information required to send an outgoing IP multicast packet.
old-location: mib\mib_ipmcast_oif.htm
old-project: mib
ms.assetid: 4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_IPMCAST_OIF, *PMIB_IPMCAST_OIF_W2K, MIB_IPMCAST_OIF, MIB_IPMCAST_OIF structure [MIB], MIB_IPMCAST_OIF_W2K, PMIB_IPMCAST_OIF, PMIB_IPMCAST_OIF structure pointer [MIB], _MIB_IPMCAST_OIF_W2K, _mpr_mib_ipmcast_oif, ipmib/MIB_IPMCAST_OIF, ipmib/PMIB_IPMCAST_OIF, iprtrmib/MIB_IPMCAST_OIF, iprtrmib/PMIB_IPMCAST_OIF, mib.mib_ipmcast_oif, rras.mib_ipmcast_oif"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MIB_IPMCAST_OIF_W2K, *PMIB_IPMCAST_OIF_W2K
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPMCAST_OIF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_IPMCAST_OIF_W2K structure


## -description


The 
<b>MIB_IPMCAST_OIF</b> structure stores the information required to send an outgoing IP multicast packet.


## -struct-fields




### -field dwOutIfIndex

The index of the interface on which to send the outgoing IP multicast packet.


### -field dwNextHopAddr

The destination address for the outgoing IPv4 multicast packet.


### -field pvReserved

Reserved. This member should be <b>NULL</b>.


### -field dwReserved

Reserved. This member should be zero.


## -remarks



The <b>MIB_IPMCAST_MFE</b> structure is used by the <a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>. The <b>MIB_IPMCAST_OIF</b> structure is retrieved as a member of the <b>MIB_IPMCAST_MFE</b> structure  using the <a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a> function.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a>



<a href="https://msdn.microsoft.com/0d1a2396-883b-4ca5-b8a0-11a3d3575a61">MIB_IPMCAST_OIF_STATS</a>



<a href="https://msdn.microsoft.com/15b1b096-9044-4983-9039-e7a13c2cca25">MgmGetMfe</a>



<a href="https://msdn.microsoft.com/d4374ced-06ea-49dd-8f52-0d06612aa4c3">Multicast Group Manager functions</a>
 

 

