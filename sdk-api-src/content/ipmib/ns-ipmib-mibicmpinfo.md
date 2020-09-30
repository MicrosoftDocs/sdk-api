---
UID: NS:ipmib._MIBICMPINFO
title: MIBICMPINFO (ipmib.h)
description: Contains Internet Control Message Protocol (ICMP) statistics for a particular computer.
helpviewer_keywords: ["MIBICMPINFO","MIBICMPINFO structure [MIB]","_mpr_mibicmpinfo","ipmib/MIBICMPINFO","iprtrmib/MIBICMPINFO","mib.mibicmpinfo","rras.mibicmpinfo"]
old-location: mib\mibicmpinfo.htm
tech.root: MIB
ms.assetid: 547da10e-3490-44d2-9142-0caed041503b
ms.date: 12/05/2018
ms.keywords: MIBICMPINFO, MIBICMPINFO structure [MIB], _mpr_mibicmpinfo, ipmib/MIBICMPINFO, iprtrmib/MIBICMPINFO, mib.mibicmpinfo, rras.mibicmpinfo
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
req.typenames: MIBICMPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIBICMPINFO
 - ipmib/_MIBICMPINFO
 - MIBICMPINFO
 - ipmib/MIBICMPINFO
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
 - MIBICMPINFO
---

# MIBICMPINFO structure


## -description

The 
<b>MIBICMPINFO</b> structure contains Internet Control Message Protocol (ICMP) statistics for a particular computer.

## -struct-fields

### -field icmpInStats

An 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a> structure that contains the statistics for incoming ICMP messages.

### -field icmpOutStats

An 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a> structure that contains the statistics for outgoing ICMP messages.

## -remarks

Two 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a> structures are required to hold all the ICMP statistics for a given computer. One 
<b>MIBICMPSTATS</b> structure contains the statistics for incoming ICMP messages. The other contains the statistics for outgoing ICMP messages. For this reason, the 
<b>MIBICMPINFO</b> structure contains two 
<b>MIBICMPSTATS</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIBICMPINFO</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats_ex_xpsp1">MIBICMPSTATS_EX</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp">MIB_ICMP</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a>