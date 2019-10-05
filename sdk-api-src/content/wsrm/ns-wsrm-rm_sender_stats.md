---
UID: NS:wsrm._RM_SENDER_STATS
title: RM_SENDER_STATS (wsrm.h)
author: windows-sdk-content
description: Provides statistical information for a Reliable Multicast sender session. This structure is used with the RM_SENDER_STATISTICS socket option.
old-location: winsock\rm_sender_stats.htm
tech.root: WinSock
ms.assetid: 9ab6019c-459a-443d-b8e4-f7ee362e3385
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RM_SENDER_STATS, RM_SENDER_STATS structure [Winsock], winsock.rm_sender_stats, wsrm/RM_SENDER_STATS
ms.topic: struct
f1_keywords:
- wsrm/RM_SENDER_STATS
dev_langs:
 - c++
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Wsrm.h
api_name:
- RM_SENDER_STATS
targetos: Windows
req.typenames: RM_SENDER_STATS
req.redist: 
ms.custom: 19H1
---

# RM_SENDER_STATS structure


## -description


The <b>RM_SENDER_STATS</b> structure provides statistical information for a Reliable Multicast sender session. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/WinSock/socket-options">RM_SENDER_STATISTICS</a> socket option.


## -struct-fields




### -field DataBytesSent

Type: <b>ULONGULONG</b>

Number of client data bytes sent out.


### -field TotalBytesSent

Type: <b>ULONGULONG</b>

Total bytes  sent, consisting of source path message (SPM), original data (ODATA) and repair data (RDATA) sequences.


### -field NaksReceived

Type: <b>ULONGULONG</b>

Number of NAKs received.


### -field NaksReceivedTooLate

Type: <b>ULONGULONG</b>

Number of NAKs received after the send window advanced beyond the NAK'ed sequence.


### -field NumOutstandingNaks

Type: <b>ULONGULONG</b>

Number of NAKs for which responses have not been sent.


### -field NumNaksAfterRData

Type: <b>ULONGULONG</b>

Number of NAKs after repair data (RDATA) sequences were sent for which responses have not been sent.


### -field RepairPacketsSent

Type: <b>ULONGULONG</b>

Number of repair data (RDATA) packets sent.


### -field BufferSpaceAvailable

Type: <b>ULONGULONG</b>

Number of partial messages dropped.


### -field TrailingEdgeSeqId

Type: <b>ULONGULONG</b>

Oldest sequence identifier in the send window.


### -field LeadingEdgeSeqId

Type: <b>ULONGULONG</b>

Newest sequence identifier in the send window.


### -field RateKBitsPerSecOverall

Type: <b>ULONGULONG</b>

Internally calculated send rate from the beginning of the session, in kilobits per second.


### -field RateKBitsPerSecLast

Type: <b>ULONGULONG</b>

Send rate for the period specified by INTERNAL_RATE_CALCULATION_FREQUENCY.


### -field TotalODataPacketsSent

Type: <b>ULONGULONG</b>

Total original data (ODATA) packets sent.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsrm/ns-wsrm-rm_receiver_stats">RM_RECEIVER_STATS</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="https://docs.microsoft.com/windows/desktop/WinSock/socket-options">Socket
  Options</a>
 

 

