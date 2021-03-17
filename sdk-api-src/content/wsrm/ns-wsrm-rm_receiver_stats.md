---
UID: NS:wsrm._RM_RECEIVER_STATS
title: RM_RECEIVER_STATS (wsrm.h)
description: Provides statistical information for a Reliable Multicast receiver session. This structure is used with the RM_RECEIVER_STATISTICS socket option.
helpviewer_keywords: ["RM_RECEIVER_STATS","RM_RECEIVER_STATS structure [Winsock]","winsock.rm_receiver_stats","wsrm/RM_RECEIVER_STATS"]
old-location: winsock\rm_receiver_stats.htm
tech.root: WinSock
ms.assetid: 972cf340-1e0e-4add-b218-054d6998023c
ms.date: 12/05/2018
ms.keywords: RM_RECEIVER_STATS, RM_RECEIVER_STATS structure [Winsock], winsock.rm_receiver_stats, wsrm/RM_RECEIVER_STATS
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
targetos: Windows
req.typenames: RM_RECEIVER_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_RECEIVER_STATS
 - wsrm/_RM_RECEIVER_STATS
 - RM_RECEIVER_STATS
 - wsrm/RM_RECEIVER_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsrm.h
api_name:
 - RM_RECEIVER_STATS
---

# RM_RECEIVER_STATS structure


## -description

The <b>RM_RECEIVER_STATS</b> structure provides statistical information for a Reliable Multicast receiver session. This structure is used with the <a href="/windows/desktop/WinSock/socket-options">RM_RECEIVER_STATISTICS</a> socket option.

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

<a href="/windows/desktop/api/wsrm/ns-wsrm-rm_sender_stats">RM_SENDER_STATS</a>



<a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket
  Options</a>