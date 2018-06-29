---
UID: NS:ipmib._MIB_ICMP
title: "_MIB_ICMP"
author: windows-sdk-content
description: Contains the Internet Control Message Protocol (ICMP) statistics for a particular computer.
old-location: mib\mib_icmp.htm
old-project: MIB
ms.assetid: 45ccaacb-f2cd-4be5-94ef-48d4403d5f60
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_ICMP, MIB_ICMP, MIB_ICMP structure [MIB], PMIB_ICMP, PMIB_ICMP structure pointer [MIB], _MIB_ICMP, _mpr_mib_icmp, ipmib/MIB_ICMP, ipmib/PMIB_ICMP, iprtrmib/MIB_ICMP, iprtrmib/PMIB_ICMP, mib.mib_icmp, rras.mib_icmp"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MIB_ICMP, *PMIB_ICMP
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_ICMP structure


## -description


The 
<b>MIB_ICMP</b> structure contains the Internet Control Message Protocol (ICMP) statistics for a particular computer.


## -struct-fields




### -field stats

A 
<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a> structure that contains the ICMP statistics for the computer.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_ICMP</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa365934(v=VS.85).aspx">GetIcmpStatistics</a>



<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a>



<a href="https://msdn.microsoft.com/080cdd28-3e2d-4cd0-8e5a-9ec9dcb9df48">MIBICMPSTATS</a>



<a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a>



<a href="https://msdn.microsoft.com/3d2c7edc-c9e6-4db6-b7c8-07f7f01cbe0d">MIB_ICMP_EX</a>
 

 

