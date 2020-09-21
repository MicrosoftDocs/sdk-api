---
UID: NS:wtsdefs._WTS_PROTOCOL_COUNTERS
title: WTS_PROTOCOL_COUNTERS (wtsdefs.h)
description: Contains protocol performance counters.
helpviewer_keywords: ["*PWTS_PROTOCOL_COUNTERS","PWRDS_PROTOCOL_COUNTERS","PWRDS_PROTOCOL_COUNTERS structure pointer [Remote Desktop Services]","PWTS_PROTOCOL_COUNTERS","PWTS_PROTOCOL_COUNTERS structure pointer [Remote Desktop Services]","WRDS_PROTOCOL_COUNTERS","WRDS_PROTOCOL_COUNTERS structure [Remote Desktop Services]","WTS_PROTOCOL_COUNTERS","WTS_PROTOCOL_COUNTERS structure [Remote Desktop Services]","termserv.wts_protocol_counters","wtsdefs/PWRDS_PROTOCOL_COUNTERS","wtsdefs/PWTS_PROTOCOL_COUNTERS","wtsdefs/WRDS_PROTOCOL_COUNTERS","wtsdefs/WTS_PROTOCOL_COUNTERS"]
old-location: termserv\wts_protocol_counters.htm
tech.root: TermServ
ms.assetid: 118c5e12-5436-4c0a-a31d-a60c5123e384
ms.date: 12/05/2018
ms.keywords: '*PWTS_PROTOCOL_COUNTERS, PWRDS_PROTOCOL_COUNTERS, PWRDS_PROTOCOL_COUNTERS structure pointer [Remote Desktop Services], PWTS_PROTOCOL_COUNTERS, PWTS_PROTOCOL_COUNTERS structure pointer [Remote Desktop Services], WRDS_PROTOCOL_COUNTERS, WRDS_PROTOCOL_COUNTERS structure [Remote Desktop Services], WTS_PROTOCOL_COUNTERS, WTS_PROTOCOL_COUNTERS structure [Remote Desktop Services], termserv.wts_protocol_counters, wtsdefs/PWRDS_PROTOCOL_COUNTERS, wtsdefs/PWTS_PROTOCOL_COUNTERS, wtsdefs/WRDS_PROTOCOL_COUNTERS, wtsdefs/WTS_PROTOCOL_COUNTERS'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_PROTOCOL_COUNTERS, *PWTS_PROTOCOL_COUNTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_PROTOCOL_COUNTERS
 - wtsdefs/_WTS_PROTOCOL_COUNTERS
 - PWTS_PROTOCOL_COUNTERS
 - wtsdefs/PWTS_PROTOCOL_COUNTERS
 - WTS_PROTOCOL_COUNTERS
 - wtsdefs/WTS_PROTOCOL_COUNTERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_PROTOCOL_COUNTERS
---

# WTS_PROTOCOL_COUNTERS structure


## -description

Contains protocol performance counters.

## -struct-fields

### -field WdBytes

The number of bytes sent and received.

### -field WdFrames

The number of frames sent and received.

### -field WaitForOutBuf

The number of times the protocol waited for an output buffer to become available.

### -field Frames

Transport driver number of frames sent and received.

### -field Bytes

Transport driver number of bytes sent and received.

### -field CompressedBytes

The number of compressed bytes.

### -field CompressFlushes

The number of compressed flushes. A compressed flush occurs when compression for a packet fails and is replaced by the original uncompressed packet.

### -field Errors

The number of packets that were in error during the session.

### -field Timeouts

The number of timeouts during the session.

### -field AsyncFramingError

The number of asynchronous framing errors during the session.

### -field AsyncOverrunError

The number of asynchronous overrun errors during the session.

### -field AsyncOverflowError

The number of asynchronous overflow errors during the session.

### -field AsyncParityError

The number of asynchronous parity errors during the session.

### -field TdErrors

The number of transport protocol errors during the session.

### -field ProtocolType

The type of the protocol.

### -field Length

The length of data in the <b>Reserved</b> field.

### -field Specific

Specifies the type of counter that can be queried. This can be <b>TShareCounters</b> or <b>Reserved</b>.

### -field Reserved

An array of protocol specific data. The maximum length can be WTS_MAX_RESERVED multiplied by the size of an unsigned long integer.

## -remarks

This structure is used by the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_protocol_status">WTS_PROTOCOL_STATUS</a> structure.