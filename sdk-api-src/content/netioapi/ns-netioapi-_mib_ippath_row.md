---
UID: NS:netioapi._MIB_IPPATH_ROW
title: "_MIB_IPPATH_ROW"
author: windows-sdk-content
description: Stores information about an IP path entry.
old-location: mib\mib_ippath_row.htm
tech.root: mib
ms.assetid: 0cfef3cb-bb96-4250-864b-2468a46ba277
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PMIB_IPPATH_ROW, MIB_IPPATH_ROW, MIB_IPPATH_ROW structure [MIB], PMIB_IPPATH_ROW, PMIB_IPPATH_ROW structure pointer [MIB], _MIB_IPPATH_ROW, mib.mib_ippath_row, netioapi/MIB_IPPATH_ROW, netioapi/PMIB_IPPATH_ROW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Netioapi.h
api_name:
 - MIB_IPPATH_ROW
product: Windows
targetos: Windows
req.typenames: MIB_IPPATH_ROW, *PMIB_IPPATH_ROW
req.redist: 
---

# _MIB_IPPATH_ROW structure


## -description


The 
<b>MIB_IPPATH_ROW</b> structure stores information about an IP path entry.


## -struct-fields




### -field Source

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The source IP address for this IP path entry. 


### -field Destination

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The destination IP address for this IP path entry. 


### -field InterfaceLuid

Type: <b>NET_LUID</b>

The locally unique identifier (LUID) for the network interface associated with this IP path entry.


### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface associated with this IP path entry. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent. 


### -field CurrentNextHop

Type: <b><a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a></b>

The current IP address of the next system or gateway en route. This member can change over the lifetime of a path. 



### -field PathMtu

Type: <b>ULONG</b>

The maximum transmission unit (MTU) size, in bytes, to the destination IP address for this IP path entry. 


### -field RttMean

Type: <b>ULONG</b>

The estimated mean round-trip time (RTT), in milliseconds, to the destination IP address for this IP path entry. 


### -field RttDeviation

Type: <b>ULONG</b>

The estimated mean deviation for the round-trip time (RTT), in milliseconds, to the destination IP address for this IP path entry. 


### -field LastReachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes the  destination IP address is
                     reachable after having received a reachability
                     confirmation. 


### -field LastUnreachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes the destination IP address is
                     unreachable after not having received a reachability
                     confirmation. 


### -field IsReachable

Type: <b>BOOLEAN</b>

A value that indicates if the destination IP address is reachable for this IP path entry.


### -field LinkTransmitSpeed

Type: <b>ULONG64</b>

The estimated speed in bits per second of the transmit link to the destination IP address for this IP path entry. 



### -field LinkReceiveSpeed

Type: <b>ULONG64</b>

The estimated speed in bits per second of the receive link from the destination IP address for this IP path entry. 



## -remarks



The <b>MIB_IPPATH_ROW</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a> function enumerates the IP path entries on a local system and returns this information in a <a href="https://msdn.microsoft.com/f18aff3c-a7b5-40fa-9308-5bd8821c77e2">MIB_IPPATH_TABLE</a> structure as an array of <b>MIB_IPPATH_ROW</b> entries. 



The <a href="https://msdn.microsoft.com/8ad43a1d-428a-41cc-bba8-5eec7f87c11f">GetIpPathEntry</a> function retrieves a single IP path entry and returns this information in a <a href="https://msdn.microsoft.com/f18aff3c-a7b5-40fa-9308-5bd8821c77e2">MIB_IPPATH_TABLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/3b28e0cd-9cab-41ca-b58c-7632768318c2">FlushIpPathTable</a>



<a href="https://msdn.microsoft.com/8ad43a1d-428a-41cc-bba8-5eec7f87c11f">GetIpPathEntry</a>



<a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/f18aff3c-a7b5-40fa-9308-5bd8821c77e2">MIB_IPPATH_TABLE</a>



<a href="https://msdn.microsoft.com/7278dcb4-65c6-4aea-a474-cb7fae4d7672">SOCKADDR_INET</a>
 

 

