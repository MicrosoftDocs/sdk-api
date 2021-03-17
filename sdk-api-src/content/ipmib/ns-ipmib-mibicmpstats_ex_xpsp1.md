---
UID: NS:ipmib._MIBICMPSTATS_EX_XPSP1
title: MIBICMPSTATS_EX_XPSP1 (ipmib.h)
description: Contains extended statistics for either incoming or outgoing Internet Control Message Protocol (ICMP) messages on a particular computer.
helpviewer_keywords: ["*PMIBICMPSTATS_EX","*PMIBICMPSTATS_EX_XPSP1","MIBICMPSTATS_EX","MIBICMPSTATS_EX structure [MIB]","MIBICMPSTATS_EX_XPSP1","PMIBICMPSTATS_EX","PMIBICMPSTATS_EX structure pointer [MIB]","ipmib/MIBICMPSTATS_EX","ipmib/PMIBICMPSTATS_EX","iprtrmib/MIBICMPSTATS_EX","iprtrmib/PMIBICMPSTATS_EX","mib.mibicmpstats_ex","rras.mibicmpstats_ex"]
old-location: mib\mibicmpstats_ex.htm
tech.root: MIB
ms.assetid: d97921f8-8be0-4a14-887f-aaafcb82eb1f
ms.date: 12/05/2018
ms.keywords: '*PMIBICMPSTATS_EX, *PMIBICMPSTATS_EX_XPSP1, MIBICMPSTATS_EX, MIBICMPSTATS_EX structure [MIB], MIBICMPSTATS_EX_XPSP1, PMIBICMPSTATS_EX, PMIBICMPSTATS_EX structure pointer [MIB], ipmib/MIBICMPSTATS_EX, ipmib/PMIBICMPSTATS_EX, iprtrmib/MIBICMPSTATS_EX, iprtrmib/PMIBICMPSTATS_EX, mib.mibicmpstats_ex, rras.mibicmpstats_ex'
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
req.typenames: MIBICMPSTATS_EX_XPSP1, *PMIBICMPSTATS_EX_XPSP1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIBICMPSTATS_EX_XPSP1
 - ipmib/_MIBICMPSTATS_EX_XPSP1
 - PMIBICMPSTATS_EX_XPSP1
 - ipmib/PMIBICMPSTATS_EX_XPSP1
 - MIBICMPSTATS_EX_XPSP1
 - ipmib/MIBICMPSTATS_EX_XPSP1
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
 - MIBICMPSTATS_EX
---

# MIBICMPSTATS_EX_XPSP1 structure


## -description

The 
<b>MIBICMPSTATS_EX</b> structure contains extended statistics for either incoming or outgoing Internet Control Message Protocol (ICMP) messages on a particular computer.

## -struct-fields

### -field dwMsgs

Type: <b>DWORD</b>

Specifies the number of messages received or sent.

### -field dwErrors

Type: <b>DWORD</b>

 The number of errors received or sent.

### -field rgdwTypeCount

Type: <b>DWORD[256]</b>

The type count.

## -remarks

Two 
<b>MIBICMPSTATS_EX</b> structures are required to hold all the extended ICMP statistics for a given computer. One 
<b>MIBICMPSTATS_EX</b> structure contains the extended statistics for incoming ICMP messages. The other contains the extended statistics for outgoing ICMP messages. For this reason, the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a> structure contains two 
<b>MIBICMPSTATS_EX</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIBICMPSTATS_EX</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpinfo">MIBICMPINFO</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats">MIBICMPSTATS</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp">MIB_ICMP</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a>