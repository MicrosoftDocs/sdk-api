---
UID: NS:ipmib._MIB_ICMP_EX_XPSP1
title: MIB_ICMP_EX_XPSP1
author: windows-sdk-content
description: Contains the extended Internet Control Message Protocol (ICMP) statistics for a particular computer.
old-location: mib\mib_icmp_ex.htm
tech.root: MIB
ms.assetid: 3d2c7edc-c9e6-4db6-b7c8-07f7f01cbe0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMIB_ICMP_EX, *PMIB_ICMP_EX_XPSP1, MIB_ICMP_EX, MIB_ICMP_EX structure [MIB], MIB_ICMP_EX_XPSP1, PMIB_ICMP_EX, PMIB_ICMP_EX structure pointer [MIB], ipmib/MIB_ICMP_EX, ipmib/PMIB_ICMP_EX, iprtrmib/MIB_ICMP_EX, iprtrmib/PMIB_ICMP_EX, mib.mib_icmp_ex, rras.mib_icmp_ex"
ms.topic: struct
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - MIB_ICMP_EX
product: Windows
targetos: Windows
req.typenames: MIB_ICMP_EX_XPSP1, *PMIB_ICMP_EX_XPSP1
req.redist: 
---

# MIB_ICMP_EX_XPSP1 structure


## -description


The 
<b>MIB_ICMP_EX</b> structure contains the extended Internet Control Message Protocol (ICMP) statistics for a particular computer.


## -struct-fields




### -field icmpInStats

Specifies an <a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a> structure that contains the extended statistics for incoming ICMP messages.


### -field icmpOutStats

Specifies an <a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a> structure that contains the extended statistics for outgoing ICMP messages.


## -remarks



Two 
<a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a> structures are required to hold all the extended ICMP statistics for a given computer. One 
<b>MIBICMPSTATS_EX</b> structure contains the extended statistics for incoming ICMP messages. The other contains the extended statistics for outgoing ICMP messages. For this reason, the 
<b>MIB_ICMP_EX</b> structure contains two 
<b>MIBICMPSTATS_EX</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_ICMP_EX</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="_iphlp_geticmpstatistics">GetIcmpStatistics</a>



<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a>



<a href="https://msdn.microsoft.com/080cdd28-3e2d-4cd0-8e5a-9ec9dcb9df48">MIBICMPSTATS</a>



<a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a>



<a href="https://msdn.microsoft.com/45ccaacb-f2cd-4be5-94ef-48d4403d5f60">MIB_ICMP</a>
 

 

