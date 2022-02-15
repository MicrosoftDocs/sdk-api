---
UID: NE:tcpestats._TCP_BOOLEAN_OPTIONAL
title: TCP_BOOLEAN_OPTIONAL (tcpestats.h)
description: Defines the states that a caller can specify when updating a member in the read/write information for a TCP connection.
helpviewer_keywords: ["*PTCP_BOOLEAN_OPTIONAL","TCP_BOOLEAN_OPTIONAL","TCP_BOOLEAN_OPTIONAL enumeration [IP Helper]","TcpBoolOptDisabled","TcpBoolOptEnabled","TcpBoolOptUnchanged","iphlp.tcp_boolean_optional","tcpestats/TCP_BOOLEAN_OPTIONAL","tcpestats/TcpBoolOptDisabled","tcpestats/TcpBoolOptEnabled","tcpestats/TcpBoolOptUnchanged"]
old-location: iphlp\tcp_boolean_optional.htm
tech.root: IpHlp
ms.assetid: 68f8f797-06fb-4286-88bc-220c54977575
ms.date: 12/05/2018
ms.keywords: '*PTCP_BOOLEAN_OPTIONAL, TCP_BOOLEAN_OPTIONAL, TCP_BOOLEAN_OPTIONAL enumeration [IP Helper], TcpBoolOptDisabled, TcpBoolOptEnabled, TcpBoolOptUnchanged, iphlp.tcp_boolean_optional, tcpestats/TCP_BOOLEAN_OPTIONAL, tcpestats/TcpBoolOptDisabled, tcpestats/TcpBoolOptEnabled, tcpestats/TcpBoolOptUnchanged'
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
req.typenames: TCP_BOOLEAN_OPTIONAL, *PTCP_BOOLEAN_OPTIONAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_BOOLEAN_OPTIONAL
 - tcpestats/_TCP_BOOLEAN_OPTIONAL
 - PTCP_BOOLEAN_OPTIONAL
 - tcpestats/PTCP_BOOLEAN_OPTIONAL
 - TCP_BOOLEAN_OPTIONAL
 - tcpestats/TCP_BOOLEAN_OPTIONAL
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
 - TCP_BOOLEAN_OPTIONAL
---

# TCP_BOOLEAN_OPTIONAL enumeration


## -description

The <b>TCP_BOOLEAN_OPTIONAL</b> enumeration defines the states that a caller can specify when updating a member in the read/write information for a TCP connection.

## -enum-fields

### -field TcpBoolOptDisabled:0

The option should be disabled.

### -field TcpBoolOptEnabled

The option should be enabled.

### -field TcpBoolOptUnchanged:-1

The option should be unchanged.

## -remarks

The <b>TCP_BOOLEAN_OPTIONAL</b> enumeration is defined on Windows Vista and later. 

The collection of extended statistics on a TCP connection are enabled and disabled using calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> functions where the type of extended statistics specified is one of values from the <a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a> enumeration type. A value from the <b>TCP_BOOLEAN_OPTIONAL</b> enumeration is used to specify how a member in the <a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a> structure should be updated to enable or disable extended statistics on a TCP connection for bandwidth estimation.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ns-tcpestats-tcp_estats_bandwidth_rw_v0">TCP_ESTATS_BANDWIDTH_RW_v0</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>
