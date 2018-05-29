---
UID: NS:wsrm._RM_SENDER_STATS
title: "_RM_SENDER_STATS"
author: windows-sdk-content
description: Provides statistical information for a Reliable Multicast sender session. This structure is used with the RM_SENDER_STATISTICS socket option.
old-location: winsock\rm_sender_stats.htm
old-project: WinSock
ms.assetid: 9ab6019c-459a-443d-b8e4-f7ee362e3385
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: RM_SENDER_STATS, RM_SENDER_STATS structure [Winsock], _RM_SENDER_STATS, winsock.rm_sender_stats, wsrm/RM_SENDER_STATS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RM_SENDER_STATS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsrm.h
api_name:
-	RM_SENDER_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _RM_SENDER_STATS structure


## -description


The <b>RM_SENDER_STATS</b> structure provides statistical information for a Reliable Multicast sender session. This structure is used with the <a href="socket_options.htm">RM_SENDER_STATISTICS</a> socket option.


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




<a href="https://msdn.microsoft.com/972cf340-1e0e-4add-b218-054d6998023c">RM_RECEIVER_STATS</a>



<a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">Reliable Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket
  Options</a>
 

 

