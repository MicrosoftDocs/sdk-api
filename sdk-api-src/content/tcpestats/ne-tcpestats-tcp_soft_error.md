---
UID: NE:tcpestats.__unnamed_enum_1
title: TCP_SOFT_ERROR (tcpestats.h)
description: Defines the reason for non-fatal or soft errors recorded on a TCP connection.
helpviewer_keywords: ["*PTCP_SOFT_ERROR","TCP_SOFT_ERROR","TCP_SOFT_ERROR enumeration [IP Helper]","TcpErrorAboveAckWindow","TcpErrorAboveDataWindow","TcpErrorAboveTsWindow","TcpErrorBelowAckWindow","TcpErrorBelowDataWindow","TcpErrorBelowTsWindow","TcpErrorDataChecksumError","TcpErrorDataLengthError","TcpErrorMaxSoftError","TcpErrorNone","iphlp.tcp_soft_error","tcpestats/TCP_SOFT_ERROR","tcpestats/TcpErrorAboveAckWindow","tcpestats/TcpErrorAboveDataWindow","tcpestats/TcpErrorAboveTsWindow","tcpestats/TcpErrorBelowAckWindow","tcpestats/TcpErrorBelowDataWindow","tcpestats/TcpErrorBelowTsWindow","tcpestats/TcpErrorDataChecksumError","tcpestats/TcpErrorDataLengthError","tcpestats/TcpErrorMaxSoftError","tcpestats/TcpErrorNone"]
old-location: iphlp\tcp_soft_error.htm
tech.root: IpHlp
ms.assetid: dd179e9b-86e6-48e8-bb4b-05d69b9794b2
ms.date: 12/05/2018
ms.keywords: '*PTCP_SOFT_ERROR, TCP_SOFT_ERROR, TCP_SOFT_ERROR enumeration [IP Helper], TcpErrorAboveAckWindow, TcpErrorAboveDataWindow, TcpErrorAboveTsWindow, TcpErrorBelowAckWindow, TcpErrorBelowDataWindow, TcpErrorBelowTsWindow, TcpErrorDataChecksumError, TcpErrorDataLengthError, TcpErrorMaxSoftError, TcpErrorNone, iphlp.tcp_soft_error, tcpestats/TCP_SOFT_ERROR, tcpestats/TcpErrorAboveAckWindow, tcpestats/TcpErrorAboveDataWindow, tcpestats/TcpErrorAboveTsWindow, tcpestats/TcpErrorBelowAckWindow, tcpestats/TcpErrorBelowDataWindow, tcpestats/TcpErrorBelowTsWindow, tcpestats/TcpErrorDataChecksumError, tcpestats/TcpErrorDataLengthError, tcpestats/TcpErrorMaxSoftError, tcpestats/TcpErrorNone'
req.header: tcpestats.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TCP_SOFT_ERROR, *PTCP_SOFT_ERROR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTCP_SOFT_ERROR
 - tcpestats/PTCP_SOFT_ERROR
 - TCP_SOFT_ERROR
 - tcpestats/TCP_SOFT_ERROR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpestats.h
api_name:
 - TCP_SOFT_ERROR
---

# TCP_SOFT_ERROR enumeration


## -description

The <b>TCP_SOFT_ERROR</b> enumeration defines the reason for non-fatal or soft errors recorded on a TCP connection.

## -enum-fields

### -field TcpErrorNone:0

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
           segment is sent).  This error is applicable to TCP connections that use the TCP Timestamps option (TSopt) defined by the IETF in RFC 1323. For more information, see <a href="https://www.ietf.org/rfc/rfc1323.txt">http://www.ietf.org/rfc/rfc1323.txt</a>. This soft error is normal for the rare case where the Protect Against Wrapped
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

The maximum possible value for the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_soft_error">TCP_SOFT_ERROR</a>_STATE enumeration type. This is not a legal value for the reason for a soft error for a TCP connection.

## -remarks

The <b>TCP_SOFT_ERROR</b> enumeration is defined on Windows Vista and later. 

The values in this enumeration are defined in the IETF draft RFC on the TCP Extended Statistics MIB. For more information, see <a href="http://tools.ietf.org/html/rfc4898">http://www.ietf.org/rfc/rfc4898.txt</a>.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>
