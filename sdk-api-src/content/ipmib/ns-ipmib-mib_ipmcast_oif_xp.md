---
UID: NS:ipmib._MIB_IPMCAST_OIF_XP
title: MIB_IPMCAST_OIF_XP (ipmib.h)
description: Stores the information required to send an outgoing IP multicast packet.
helpviewer_keywords: ["*PMIB_IPMCAST_OIF","*PMIB_IPMCAST_OIF_XP","MIB_IPMCAST_OIF","MIB_IPMCAST_OIF structure [MIB]","MIB_IPMCAST_OIF_XP","PMIB_IPMCAST_OIF","PMIB_IPMCAST_OIF structure pointer [MIB]","_mpr_mib_ipmcast_oif","ipmib/MIB_IPMCAST_OIF","ipmib/PMIB_IPMCAST_OIF","iprtrmib/MIB_IPMCAST_OIF","iprtrmib/PMIB_IPMCAST_OIF","mib.mib_ipmcast_oif","rras.mib_ipmcast_oif"]
old-location: mib\mib_ipmcast_oif.htm
tech.root: MIB
ms.assetid: 4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPMCAST_OIF, *PMIB_IPMCAST_OIF_XP, MIB_IPMCAST_OIF, MIB_IPMCAST_OIF structure [MIB], MIB_IPMCAST_OIF_XP, PMIB_IPMCAST_OIF, PMIB_IPMCAST_OIF structure pointer [MIB], _mpr_mib_ipmcast_oif, ipmib/MIB_IPMCAST_OIF, ipmib/PMIB_IPMCAST_OIF, iprtrmib/MIB_IPMCAST_OIF, iprtrmib/PMIB_IPMCAST_OIF, mib.mib_ipmcast_oif, rras.mib_ipmcast_oif'
f1_keywords:
- ipmib/MIB_IPMCAST_OIF
dev_langs:
- c++
req.header: ipmib.h
req.include-header: Iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: MIB_IPMCAST_OIF_XP, *PMIB_IPMCAST_OIF_XP
req.redist: 
ms.custom: 19H1
---

# MIB_IPMCAST_OIF_XP structure


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



The <b>MIB_IPMCAST_MFE</b> structure is used by the <a href="https://docs.microsoft.com/windows/desktop/RRAS/multicast-group-manager-functions">Multicast Group Manager functions</a>. The <b>MIB_IPMCAST_OIF</b> structure is retrieved as a member of the <b>MIB_IPMCAST_MFE</b> structure  using the <a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetmfe">MgmGetMfe</a> function.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Server 2008and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_mfe">MIB_IPMCAST_MFE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipmib/ns-ipmib-mib_ipmcast_oif_stats_lh">MIB_IPMCAST_OIF_STATS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mgm/nf-mgm-mgmgetmfe">MgmGetMfe</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/multicast-group-manager-functions">Multicast Group Manager functions</a>
 

 

