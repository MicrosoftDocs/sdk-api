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

# _MIBICMPSTATS structure


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
<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a> structure contains two 
<b>MIBICMPSTATS</b> structures.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIBICMPSTATS</b> structure is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/547da10e-3490-44d2-9142-0caed041503b">MIBICMPINFO</a>



<a href="https://msdn.microsoft.com/d97921f8-8be0-4a14-887f-aaafcb82eb1f">MIBICMPSTATS_EX</a>



<a href="https://msdn.microsoft.com/45ccaacb-f2cd-4be5-94ef-48d4403d5f60">MIB_ICMP</a>



<a href="https://msdn.microsoft.com/3d2c7edc-c9e6-4db6-b7c8-07f7f01cbe0d">MIB_ICMP_EX</a>
 

 

