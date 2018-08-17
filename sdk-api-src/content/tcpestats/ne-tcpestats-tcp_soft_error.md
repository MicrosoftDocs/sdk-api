---
UID: NE:tcpestats.TCP_SOFT_ERROR
title: TCP_SOFT_ERROR
author: windows-sdk-content
description: Defines the reason for non-fatal or soft errors recorded on a TCP connection.
old-location: iphlp\tcp_soft_error.htm
old-project: iphlp
ms.assetid: dd179e9b-86e6-48e8-bb4b-05d69b9794b2
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PTCP_SOFT_ERROR, TCP_SOFT_ERROR, TCP_SOFT_ERROR enumeration [IP Helper], TcpErrorAboveAckWindow, TcpErrorAboveDataWindow, TcpErrorAboveTsWindow, TcpErrorBelowAckWindow, TcpErrorBelowDataWindow, TcpErrorBelowTsWindow, TcpErrorDataChecksumError, TcpErrorDataLengthError, TcpErrorMaxSoftError, TcpErrorNone, iphlp.tcp_soft_error, tcpestats/TCP_SOFT_ERROR, tcpestats/TcpErrorAboveAckWindow, tcpestats/TcpErrorAboveDataWindow, tcpestats/TcpErrorAboveTsWindow, tcpestats/TcpErrorBelowAckWindow, tcpestats/TcpErrorBelowDataWindow, tcpestats/TcpErrorBelowTsWindow, tcpestats/TcpErrorDataChecksumError, tcpestats/TcpErrorDataLengthError, tcpestats/TcpErrorMaxSoftError, tcpestats/TcpErrorNone"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tcpestats.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TCP_SOFT_ERROR, *PTCP_SOFT_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpestats.h
api_name:
 - TCP_SOFT_ERROR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TCP_SOFT_ERROR enumeration


## -description


The <b>TCP_SOFT_ERROR</b> enumeration defines the reason for non-fatal or soft errors recorded on a TCP connection.


## -enum-fields




### -field TcpErrorNone

No soft errors have occurred.


### -field TcpErrorBelowDataWindow

All data in the segment is below
           the send unacknowledged (SND.UNA) sequence number. This soft error is normal for keep-alives and zero window probes.


### -field TcpErrorAboveDataWindow

Some data in the segment is above
           send window (SND.WND) size. This soft error indicates an implementation bug or possible
           attack.


### -field TcpErrorBelowAckWindow

An ACK was received below the SND.UNA sequence number. This soft error indicates that the
           return path is reordering ACKs.


### -field TcpErrorAboveAckWindow

An ACK was received for data that we have not sent.
           This soft error indicates an implementation bug or possible attack.


### -field TcpErrorBelowTsWindow

The Timestamp Echo Reply (TSecr) on the segment is older than the
           current TS.Recent (a timestamp to be echoed in TSecr whenever a
           segment is sent).  This error is applicable to TCP connections that use the TCP Timestamps option (TSopt) defined by the IETF in RFC 1323. For more information, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=84406">http://www.ietf.org/rfc/rfc1323.txt</a>. This soft error is normal for the rare case where the Protect Against Wrapped
   Sequences numbers (PAWS)
           mechanism detects data reordered by the network.


### -field TcpErrorAboveTsWindow

The TSecr on the segment is newer than the
           current TS.Recent. This soft error indicates an implementation bug or
           possible attack.


### -field TcpErrorDataChecksumError

An incorrect TCP checksum was received. Note that this value
           is intrinsically fragile, because the header fields used to
           identify the connection may have been corrupted.


### -field TcpErrorDataLengthError

A data length error occurred. 

This value is not defined in the IETF draft RFC on the TCP Extended Statistics MIB.


### -field TcpErrorMaxSoftError

The maximum possible value for the <a href="https://msdn.microsoft.com/dd179e9b-86e6-48e8-bb4b-05d69b9794b2">TCP_SOFT_ERROR</a>_STATE enumeration type. This is not a legal value for the reason for a soft error for a TCP connection.


## -remarks



The <b>TCP_SOFT_ERROR</b> enumeration is defined on Windows Vista and later. 

The values in this enumeration are defined in the IETF draft RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=121686">http://www.ietf.org/rfc/rfc4898.txt</a>.





## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

