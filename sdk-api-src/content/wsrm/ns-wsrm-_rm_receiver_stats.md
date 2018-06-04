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

# _RM_RECEIVER_STATS structure


## -description


The <b>RM_RECEIVER_STATS</b> structure provides statistical information for a Reliable Multicast receiver session. This structure is used with the <a href="socket_options.htm">RM_RECEIVER_STATISTICS</a> socket option.


## -struct-fields




### -field NumODataPacketsReceived

Type: <b>ULONGULONG</b>

The number of original data (ODATA) sequences received.


### -field NumRDataPacketsReceived

Type: <b>ULONGULONG</b>

The number of repair data (RDATA) sequences received.


### -field NumDuplicateDataPackets

Type: <b>ULONGULONG</b>

The number of duplicate sequences received.


### -field DataBytesReceived

Type: <b>ULONGULONG</b>

The number of data bytes  received.


### -field TotalBytesReceived

Type: <b>ULONGULONG</b>

The total bytes  received, consisting of source path message (SPM), original data (ODATA) and repair data (RDATA) sequences.


### -field RateKBitsPerSecOverall

Type: <b>ULONGULONG</b>

An internally calculated receive rate from the beginning of the session, in kilobits per second.


### -field RateKBitsPerSecLast

Type: <b>ULONGULONG</b>

The receive rate for the period specified by INTERNAL_RATE_CALCULATION_FREQUENCY.


### -field TrailingEdgeSeqId

Type: <b>ULONGULONG</b>

The oldest sequence identifier in the receive window.


### -field LeadingEdgeSeqId

Type: <b>ULONGULONG</b>

The newest sequence identifier in the receive window.


### -field AverageSequencesInWindow

Type: <b>ULONGULONG</b>

The average number of sequences in the receive window.


### -field MinSequencesInWindow

Type: <b>ULONGULONG</b>

The minimum number of sequences in the receive window.


### -field MaxSequencesInWindow

Type: <b>ULONGULONG</b>

The maximum number of sequences in the receive window.


### -field FirstNakSequenceNumber

Type: <b>ULONGULONG</b>

The sequence number for the first outstanding negative acknowledgment (NAK).


### -field NumPendingNaks

Type: <b>ULONGULONG</b>

The number of sequences awaiting a NAK confirmation.


### -field NumOutstandingNaks

Type: <b>ULONGULONG</b>

The number of sequences awaiting repair data (RDATA).


### -field NumDataPacketsBuffered

Type: <b>ULONGULONG</b>

The number of packets currently buffered.


### -field TotalSelectiveNaksSent

Type: <b>ULONGULONG</b>

The number of selective NAKs sent this session.


### -field TotalParityNaksSent

Type: <b>ULONGULONG</b>

The number of parity NAKs sent this session.


## -see-also




<a href="https://msdn.microsoft.com/9ab6019c-459a-443d-b8e4-f7ee362e3385">RM_SENDER_STATS</a>



<a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">Reliable Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket
  Options</a>
 

 

