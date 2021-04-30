---
UID: NS:ipmib._MIBICMPSTATS
title: MIBICMPSTATS (ipmib.h)
description: Contains statistics for either incoming or outgoing Internet Control Message Protocol (ICMP) messages on a particular computer.
helpviewer_keywords: ["*PMIBICMPSTATS","MIBICMPSTATS","MIBICMPSTATS structure [MIB]","_mpr_mibicmpstats","ipmib/MIBICMPSTATS","iprtrmib/MIBICMPSTATS","mib.mibicmpstats","rras.mibicmpstats"]
old-location: mib\mibicmpstats.htm
tech.root: MIB
ms.assetid: 080cdd28-3e2d-4cd0-8e5a-9ec9dcb9df48
ms.date: 12/05/2018
ms.keywords: '*PMIBICMPSTATS, MIBICMPSTATS, MIBICMPSTATS structure [MIB], _mpr_mibicmpstats, ipmib/MIBICMPSTATS, iprtrmib/MIBICMPSTATS, mib.mibicmpstats, rras.mibicmpstats'
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
req.typenames: MIBICMPSTATS, *PMIBICMPSTATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIBICMPSTATS
 - ipmib/_MIBICMPSTATS
 - PMIBICMPSTATS
 - ipmib/PMIBICMPSTATS
 - MIBICMPSTATS
 - ipmib/MIBICMPSTATS
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
 - MIBICMPSTATS
---

# MIBICMPSTATS structure


## -description

The 
<b>MIBICMPSTATS</b> structure contains statistics for either incoming or outgoing Internet Control Message Protocol (ICMP) messages on a particular computer.

## -struct-fields

### -field dwMsgs

Type: <b>DWORD</b>

The number of messages received or sent.

### -field dwErrors

Type: <b>DWORD</b>

The number of errors received or sent.

### -field dwDestUnreachs

Type: <b>DWORD</b>

The number of destination-unreachable messages received or sent. A destination-unreachable message is sent to the originating computer when a datagram fails to reach its intended destination.

### -field dwTimeExcds

Type: <b>DWORD</b>

The number of time-to-live (TTL) exceeded messages received or sent. A time-to-live exceeded message is sent to the originating computer when a datagram is discarded because the number of routers it has passed through exceeds its time-to-live value.

### -field dwParmProbs

Type: <b>DWORD</b>

The number of parameter-problem messages received or sent. A parameter-problem message is sent to the originating computer when a router or host detects an error in a datagram's IP header.

### -field dwSrcQuenchs

Type: <b>DWORD</b>

The number of source quench messages received or sent. A source quench request is sent to a computer to request that it reduce its rate of packet transmission.

### -field dwRedirects

Type: <b>DWORD</b>

The number of redirect messages received or sent. A redirect message is sent to the originating computer when a better route is discovered for a datagram sent by that computer.

### -field dwEchos

Type: <b>DWORD</b>

The number of echo requests received or sent. An echo request causes the receiving computer to send an echo reply message back to the originating computer.

### -field dwEchoReps

Type: <b>DWORD</b>

The number of echo replies received or sent. A computer sends an echo reply in response to receiving an echo request message.

### -field dwTimestamps

Type: <b>DWORD</b>

The number of time-stamp requests received or sent. A time-stamp request causes the receiving computer to send a time-stamp reply back to the originating computer.

### -field dwTimestampReps

Type: <b>DWORD</b>

The number of time-stamp replies received or sent. A computer sends a time-stamp reply in response to receiving a time-stamp request. Routers can use time-stamp requests and replies to measure the transmission speed of datagrams on a network.

### -field dwAddrMasks

Type: <b>DWORD</b>

The number of address mask requests received or sent. A computer sends an address mask request to determine the number of bits in the subnet mask for its local subnet.

### -field dwAddrMaskReps

Type: <b>DWORD</b>

The number of address mask responses received or sent. A computer sends an address mask response in response to an address mask request.

## -remarks

Two 
<b>MIBICMPSTATS</b> structures are required to hold all the ICMP statistics for a given computer. One 
<b>MIBICMPSTATS</b> structure contains the statistics for incoming ICMP messages. The other contains the statistics for outgoing ICMP messages. For this reason, the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpinfo">MIBICMPINFO</a> structure contains two 
<b>MIBICMPSTATS</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIBICMPSTATS</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpinfo">MIBICMPINFO</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mibicmpstats_ex_xpsp1">MIBICMPSTATS_EX</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp">MIB_ICMP</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_icmp_ex_xpsp1">MIB_ICMP_EX</a>