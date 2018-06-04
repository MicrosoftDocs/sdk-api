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

# _MIB_ICMP_EX_XPSP1 structure


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
 

 

