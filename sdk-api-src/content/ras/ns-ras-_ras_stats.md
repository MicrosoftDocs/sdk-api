---
UID: NS:ras._RAS_STATS
title: "_RAS_STATS"
author: windows-sdk-content
description: The RAS_STATS structure stores the statistics for a single-link RAS connection, or for one of the links in a multilink RAS connection.
old-location: rras\ras_stats.htm
tech.root: rras
ms.assetid: f55852f9-fa6f-480c-9c65-d6631d5270a0
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: "*PRAS_STATS, RAS_STATS, RAS_STATS structure [RAS], _RAS_STATS, _ras_ras_stats, ras/RAS_STATS, rras.ras_stats"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RAS_STATS
product: Windows
targetos: Windows
req.typenames: RAS_STATS, *PRAS_STATS
req.redist: 
---

# _RAS_STATS structure


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




<a href="https://msdn.microsoft.com/b5c87ecd-4f21-46b5-91a3-41706907157a">RasClearConnectionStatistics</a>



<a href="https://msdn.microsoft.com/cac356a9-092c-4db2-b0a4-aaacfc514e29">RasClearLinkStatistics</a>



<a href="https://msdn.microsoft.com/2db03535-c2bd-4e04-a86f-e68fe5c1f805">RasGetConnectionStatistics</a>



<a href="https://msdn.microsoft.com/825a80c9-8023-4b7f-a303-f1eaa650e1d8">RasGetLinkStatistics</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/c20e8892-7c5e-48cc-939a-9b747fefe09d">Remote Access Service Structures</a>
 

 

