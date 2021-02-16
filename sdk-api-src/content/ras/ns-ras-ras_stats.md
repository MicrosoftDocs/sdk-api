---
UID: NS:ras._RAS_STATS
title: RAS_STATS (ras.h)
description: The RAS_STATS structure stores the statistics for a single-link RAS connection, or for one of the links in a multilink RAS connection.
helpviewer_keywords: ["*PRAS_STATS","RAS_STATS","RAS_STATS structure [RAS]","_ras_ras_stats","ras/RAS_STATS","rras.ras_stats"]
old-location: rras\ras_stats.htm
tech.root: RRAS
ms.assetid: f55852f9-fa6f-480c-9c65-d6631d5270a0
ms.date: 12/05/2018
ms.keywords: '*PRAS_STATS, RAS_STATS, RAS_STATS structure [RAS], _ras_ras_stats, ras/RAS_STATS, rras.ras_stats'
req.header: ras.h
req.include-header: 
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
req.typenames: RAS_STATS, *PRAS_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_STATS
 - ras/_RAS_STATS
 - PRAS_STATS
 - ras/PRAS_STATS
 - RAS_STATS
 - ras/RAS_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RAS_STATS
---

# RAS_STATS structure


## -description

The 
<b>RAS_STATS</b> structure stores the statistics for a single-link RAS connection, or for one of the links in a multilink RAS connection.

## -struct-fields

### -field dwSize

Specifies the version of the structure. Set this member to sizeof(<b>RAS_STATS</b>) before using the structure in a function call.

### -field dwBytesXmited

The number of bytes transmitted through this connection or link.

### -field dwBytesRcved

The number of bytes received through this connection or link.

### -field dwFramesXmited

The number frames transmitted through this connection or link.

### -field dwFramesRcved

The number of frames received through this connection or link.

### -field dwCrcErr

The number of cyclic redundancy check (CRC) errors on this connection or link.

### -field dwTimeoutErr

The number of timeout errors on this connection or link.

### -field dwAlignmentErr

The number of alignment errors on this connection or link.

### -field dwHardwareOverrunErr

The number of hardware overrun errors on this connection or link.

### -field dwFramingErr

The number of framing errors on this connection or link.

### -field dwBufferOverrunErr

The number of buffer overrun errors on this connection or link.

### -field dwCompressionRatioIn

The compression ratio for the data being received on this connection or link.

<div class="alert"><b>Note</b>  This element is only valid for a single link connection or a single link in a multilink connection.</div>
<div> </div>

### -field dwCompressionRatioOut

The compression ratio for the data being transmitted on this connection or link.

<div class="alert"><b>Note</b>  This element is only valid for a single link connection or a single link in a multilink connection.</div>
<div> </div>

### -field dwBps

The speed of the connection or link, in bits per second. 




For a single-link connection and for individual links in a multilink connection, this speed is negotiated at the time the connection or link is established.

For multilink connections, this speed is equal to the sum of the speeds of the individual links. For multilink connections, this speed varies as links are added or deleted.

This speed is not equal to the throughput of the connection or link. To calculate the average throughput, divide the number of bytes transmitted (<b>dwBytesXmited</b>) and received (<b>dwBytesRcved</b>) by the amount of time the connection or link has been up (<b>dwConnectDuration</b>).

### -field dwConnectDuration

The amount of time, in milliseconds, that the connection or link has been connected.

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rasclearconnectionstatistics">RasClearConnectionStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasclearlinkstatistics">RasClearLinkStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectionstatistics">RasGetConnectionStatistics</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetlinkstatistics">RasGetLinkStatistics</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-structures">Remote Access Service Structures</a>