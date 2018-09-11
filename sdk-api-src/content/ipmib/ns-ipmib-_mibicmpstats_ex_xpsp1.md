---
UID: NS:ipmib._MIBICMPSTATS_EX_XPSP1
title: "_MIBICMPSTATS_EX_XPSP1"
author: windows-sdk-content
description: Contains extended statistics for either incoming or outgoing Internet Control Message Protocol (ICMP) messages on a particular computer.
old-location: mib\mibicmpstats_ex.htm
tech.root: mib
ms.assetid: d97921f8-8be0-4a14-887f-aaafcb82eb1f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIBICMPSTATS_EX, *PMIBICMPSTATS_EX_XPSP1, MIBICMPSTATS_EX, MIBICMPSTATS_EX structure [MIB], MIBICMPSTATS_EX_XPSP1, PMIBICMPSTATS_EX, PMIBICMPSTATS_EX structure pointer [MIB], _MIBICMPSTATS_EX_XPSP1, ipmib/MIBICMPSTATS_EX, ipmib/PMIBICMPSTATS_EX, iprtrmib/MIBICMPSTATS_EX, iprtrmib/PMIBICMPSTATS_EX, mib.mibicmpstats_ex, rras.mibicmpstats_ex"
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
 - MIBICMPSTATS_EX
product: Windows
targetos: Windows
req.typenames: MIBICMPSTATS_EX_XPSP1, *PMIBICMPSTATS_EX_XPSP1
req.redist: 
---

# _MIBICMPSTATS_EX_XPSP1 structure


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
<a href="https://msdn.microsoft.com/3d2c7edc-c9e6-4db6-b7c8-07f7f01cbe0d">MIB_ICMP_EX</a> structure contains two 
<b>MIBICMPSTATS_EX</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIBICMPSTATS_EX</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a>



<a href="https://msdn.microsoft.com/080cdd28-3e2d-4cd0-8e5a-9ec9dcb9df48">MIBICMPSTATS</a>



<a href="https://msdn.microsoft.com/45ccaacb-f2cd-4be5-94ef-48d4403d5f60">MIB_ICMP</a>



<a href="https://msdn.microsoft.com/3d2c7edc-c9e6-4db6-b7c8-07f7f01cbe0d">MIB_ICMP_EX</a>
 

 

