---
UID: NS:tcpmib._MIB_TCP6ROW_OWNER_MODULE
title: MIB_TCP6ROW_OWNER_MODULE (tcpmib.h)
description: Contains information that describes an IPv6 TCP connection bound to a specific process ID (PID) with ownership data.
helpviewer_keywords: ["*PMIB_TCP6ROW_OWNER_MODULE","MIB_TCP6ROW_OWNER_MODULE","MIB_TCP6ROW_OWNER_MODULE structure [MIB]","MIB_TCP_STATE_CLOSED","MIB_TCP_STATE_CLOSE_WAIT","MIB_TCP_STATE_CLOSING","MIB_TCP_STATE_DELETE_TCB","MIB_TCP_STATE_ESTAB","MIB_TCP_STATE_FIN_WAIT1","MIB_TCP_STATE_FIN_WAIT2","MIB_TCP_STATE_LAST_ACK","MIB_TCP_STATE_LISTEN","MIB_TCP_STATE_SYN_RCVD","MIB_TCP_STATE_SYN_SENT","MIB_TCP_STATE_TIME_WAIT","PMIB_TCP6ROW_OWNER_MODULE","PMIB_TCP6ROW_OWNER_MODULE structure pointer [MIB]","iprtrmib/MIB_TCP6ROW_OWNER_MODULE","iprtrmib/PMIB_TCP6ROW_OWNER_MODULE","mib.mib_tcp6row_owner_module","tcpmib/MIB_TCP6ROW_OWNER_MODULE","tcpmib/PMIB_TCP6ROW_OWNER_MODULE"]
old-location: mib\mib_tcp6row_owner_module.htm
tech.root: MIB
ms.assetid: 24f2041c-0a8c-4f2c-8585-ebbb0cad394f
ms.date: 12/05/2018
ms.keywords: '*PMIB_TCP6ROW_OWNER_MODULE, MIB_TCP6ROW_OWNER_MODULE, MIB_TCP6ROW_OWNER_MODULE structure [MIB], MIB_TCP_STATE_CLOSED, MIB_TCP_STATE_CLOSE_WAIT, MIB_TCP_STATE_CLOSING, MIB_TCP_STATE_DELETE_TCB, MIB_TCP_STATE_ESTAB, MIB_TCP_STATE_FIN_WAIT1, MIB_TCP_STATE_FIN_WAIT2, MIB_TCP_STATE_LAST_ACK, MIB_TCP_STATE_LISTEN, MIB_TCP_STATE_SYN_RCVD, MIB_TCP_STATE_SYN_SENT, MIB_TCP_STATE_TIME_WAIT, PMIB_TCP6ROW_OWNER_MODULE, PMIB_TCP6ROW_OWNER_MODULE structure pointer [MIB], iprtrmib/MIB_TCP6ROW_OWNER_MODULE, iprtrmib/PMIB_TCP6ROW_OWNER_MODULE, mib.mib_tcp6row_owner_module, tcpmib/MIB_TCP6ROW_OWNER_MODULE, tcpmib/PMIB_TCP6ROW_OWNER_MODULE'
req.header: tcpmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: MIB_TCP6ROW_OWNER_MODULE, *PMIB_TCP6ROW_OWNER_MODULE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_TCP6ROW_OWNER_MODULE
 - tcpmib/_MIB_TCP6ROW_OWNER_MODULE
 - PMIB_TCP6ROW_OWNER_MODULE
 - tcpmib/PMIB_TCP6ROW_OWNER_MODULE
 - MIB_TCP6ROW_OWNER_MODULE
 - tcpmib/MIB_TCP6ROW_OWNER_MODULE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tcpmib.h
 - Iprtrmib.h
api_name:
 - MIB_TCP6ROW_OWNER_MODULE
---

# MIB_TCP6ROW_OWNER_MODULE structure


## -description

The <b>MIB_TCP6ROW_OWNER_MODULE</b> structure contains information that describes an IPv6 TCP connection bound to a specific process ID (PID) with ownership data.

## -struct-fields

### -field ucLocalAddr

Type: <b>UCHAR[16]</b>

The IPv6 address for the local endpoint of the TCP connection on the local computer. A value of zero indicates the listener  can accept a connection on any interface.

### -field dwLocalScopeId

Type: <b>DWORD</b>

The scope ID in network byte order for the local IPv6 address.

### -field dwLocalPort

Type: <b>DWORD</b>

The port number in network byte order for the local endpoint of the TCP connection on the local computer.

### -field ucRemoteAddr

Type: <b>UCHAR[16]</b>

The IPv6 address of the remote endpoint of the TCP connection on the remote computer. When the <b>dwState</b> member is <b>MIB_TCP_STATE_LISTEN</b>, this value has no meaning.

### -field dwRemoteScopeId

Type: <b>DWORD</b>

The scope ID in network byte order for the remote IPv6 address.

### -field dwRemotePort

Type: <b>DWORD</b>

The port number in network byte order for the remote endpoint of the TCP connection on the remote computer.

### -field dwState

Type: <b>DWORD</b>

The state of the TCP connection. This member can be one of the values from the <b>MIB_TCP_STATE</b> enumeration defined in the <i>Tcpmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSED"></a><a id="mib_tcp_state_closed"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSED state that represents no connection state at all.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_LISTEN"></a><a id="mib_tcp_state_listen"></a><dl>
<dt><b>MIB_TCP_STATE_LISTEN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the LISTEN state waiting for a connection request from any remote
    TCP and port.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_SYN_SENT"></a><a id="mib_tcp_state_syn_sent"></a><dl>
<dt><b>MIB_TCP_STATE_SYN_SENT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the SYN-SENT state waiting for a matching connection request
    after having sent a connection request (SYN packet).

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_SYN_RCVD"></a><a id="mib_tcp_state_syn_rcvd"></a><dl>
<dt><b>MIB_TCP_STATE_SYN_RCVD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the SYN-RECEIVED state waiting for a confirming connection
    request acknowledgment after having both received and sent a
    connection request (SYN packet).

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_ESTAB"></a><a id="mib_tcp_state_estab"></a><dl>
<dt><b>MIB_TCP_STATE_ESTAB</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the ESTABLISHED state that represents an open connection, data received can be
    delivered to the user.  This is the normal state for the data transfer phase
    of the TCP connection.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_FIN_WAIT1"></a><a id="mib_tcp_state_fin_wait1"></a><dl>
<dt><b>MIB_TCP_STATE_FIN_WAIT1</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The TCP connection is FIN-WAIT-1 state waiting for a connection termination request
    from the remote TCP, or an acknowledgment of the connection
    termination request previously sent.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_FIN_WAIT2"></a><a id="mib_tcp_state_fin_wait2"></a><dl>
<dt><b>MIB_TCP_STATE_FIN_WAIT2</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The TCP connection is FIN-WAIT-1 state waiting for a connection termination request
    from the remote TCP.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSE_WAIT"></a><a id="mib_tcp_state_close_wait"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSE_WAIT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSE-WAIT state waiting for a connection termination request
    from the local user.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_CLOSING"></a><a id="mib_tcp_state_closing"></a><dl>
<dt><b>MIB_TCP_STATE_CLOSING</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the CLOSING state waiting for a connection termination request
    acknowledgment from the remote TCP.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_LAST_ACK"></a><a id="mib_tcp_state_last_ack"></a><dl>
<dt><b>MIB_TCP_STATE_LAST_ACK</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the LAST-ACK state waiting for an acknowledgment of the
    connection termination request previously sent to the remote TCP
    (which includes an acknowledgment of its connection termination
    request). 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_TIME_WAIT"></a><a id="mib_tcp_state_time_wait"></a><dl>
<dt><b>MIB_TCP_STATE_TIME_WAIT</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the TIME-WAIT state waiting for enough time to pass to be sure
    the remote TCP received the acknowledgment of its connection
    termination request.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_TCP_STATE_DELETE_TCB"></a><a id="mib_tcp_state_delete_tcb"></a><dl>
<dt><b>MIB_TCP_STATE_DELETE_TCB</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The TCP connection is in the delete TCB state that represents the deletion of the Transmission Control Block (TCB), a data structure used to maintain information on each TCP entry.

</td>
</tr>
</table>

### -field dwOwningPid

Type: <b>DWORD</b>

The PID of the local process that issued a context bind for this TCP connection.

### -field liCreateTimestamp

Type: <b>LARGE_INTEGER</b>

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that indicates when the context bind operation that created this TCP connection occurred.

### -field OwningModuleInfo

Type: <b>ULONGLONG[TCPIP_OWNING_MODULE_SIZE]</b>

An array of opaque data that contains ownership information.

## -remarks

The <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a> structure is returned by a call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a> with the <i>TableClass</i> parameter set to a  <b>TCP_TABLE_OWNER_MODULE_LISTENER</b>, <b>TCP_TABLE_OWNER_MODULE_CONNECTIONS</b>, or <b>TCP_TABLE_OWNER_MODULE_ALL</b> from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration and the <i>ulAf</i> parameter set to <b>AF_INET6</b>. The <b>MIB_TCP6TABLE_OWNER_MODULE</b> structure contains an array of <b>MIB_TCP6ROW_OWNER_MODULE</b> structures.

  The <b>dwState</b> member indicates the state of the TCP entry in a TCP state diagram. A TCP connection progresses through a series of states during its
  lifetime.  The states are:  LISTEN, SYN-SENT, SYN-RECEIVED,
  ESTABLISHED, FIN-WAIT-1, FIN-WAIT-2, CLOSE-WAIT, CLOSING, LAST-ACK,
  TIME-WAIT, and the fictional state CLOSED.  The CLOSED state is fictional
  because it represents the state when there is no Transmission Control Block, and therefore,
  no connection.  The TCP protocol is described in RFC 793. For more information, see 
<a href="https://www.ietf.org/rfc/rfc793.txt">http://www.ietf.org/rfc/rfc793.txt</a>. 

The <b>ucLocalAddr</b> and <b>ucRemoteAddr</b> members are stored in  a character array in network byte order. The <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a> or <a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a> functions may be used to convert the IPv6 address in the <b>ucLocalAddr</b> or <b>ucRemoteAddr</b> members to a string without loading the Windows Sockets DLL. 

The <b>dwLocalScopeId</b>, and <b>dwRemoteScopeId</b> members are in network byte order. In order to use the <b>dwLocalScopeId</b> or <b>dwRemoteScopeId</b> members, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

The <b>dwLocalPort</b> and <b>dwRemotePort</b> members are in network byte order. In order to use the <b>dwLocalPort</b> or <b>dwRemotePort</b> members, the <a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a> or <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions in Windows Sockets or similar functions may be needed. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohl">ntohl</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ntohs">ntohs</a>
