---
UID: NS:ipmib._MIB_ICMP
title: MIB_ICMP (ipmib.h)
description: Contains the Internet Control Message Protocol (ICMP) statistics for a particular computer.
helpviewer_keywords: ["*PMIB_ICMP","MIB_ICMP","MIB_ICMP structure [MIB]","PMIB_ICMP","PMIB_ICMP structure pointer [MIB]","_mpr_mib_icmp","ipmib/MIB_ICMP","ipmib/PMIB_ICMP","iprtrmib/MIB_ICMP","iprtrmib/PMIB_ICMP","mib.mib_icmp","rras.mib_icmp"]
old-location: mib\mib_icmp.htm
tech.root: MIB
ms.assetid: 45ccaacb-f2cd-4be5-94ef-48d4403d5f60
ms.date: 12/05/2018
ms.keywords: '*PMIB_ICMP, MIB_ICMP, MIB_ICMP structure [MIB], PMIB_ICMP, PMIB_ICMP structure pointer [MIB], _mpr_mib_icmp, ipmib/MIB_ICMP, ipmib/PMIB_ICMP, iprtrmib/MIB_ICMP, iprtrmib/PMIB_ICMP, mib.mib_icmp, rras.mib_icmp'
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
targetos: Windows
req.typenames: MIB_ICMP, *PMIB_ICMP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_ICMP
 - ipmib/_MIB_ICMP
 - PMIB_ICMP
 - ipmib/PMIB_ICMP
 - MIB_ICMP
 - ipmib/MIB_ICMP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_ICMP
---

# MIB_ICMP structure


## -description

The 
<b>MIB_ICMP</b> structure contains the Internet Control Message Protocol (ICMP) statistics for a particular computer.

## -struct-fields

### -field stats

A 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpinfo">MIBICMPINFO</a> structure that contains the ICMP statistics for the computer.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_ICMP</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-geticmpstatistics">GetIcmpStatistics</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpinfo">MIBICMPINFO</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats_ex_xpsp1">MIBICMPSTATS_EX</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a>