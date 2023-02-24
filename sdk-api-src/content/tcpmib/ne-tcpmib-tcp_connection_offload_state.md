---
UID: NE:tcpmib.TCP_CONNECTION_OFFLOAD_STATE
title: TCP_CONNECTION_OFFLOAD_STATE (tcpmib.h)
description: Defines the possible TCP offload states for a TCP connection.
helpviewer_keywords: ["*PTCP_CONNECTION_OFFLOAD_STATE","TCP_CONNECTION_OFFLOAD_STATE","TCP_CONNECTION_OFFLOAD_STATE enumeration [MIB]","TcpConnectionOffloadStateInHost","TcpConnectionOffloadStateMax","TcpConnectionOffloadStateOffloaded","TcpConnectionOffloadStateOffloading","TcpConnectionOffloadStateUploading","iprtrmib/TCP_CONNECTION_OFFLOAD_STATE","iprtrmib/TcpConnectionOffloadStateInHost","iprtrmib/TcpConnectionOffloadStateMax","iprtrmib/TcpConnectionOffloadStateOffloaded","iprtrmib/TcpConnectionOffloadStateOffloading","iprtrmib/TcpConnectionOffloadStateUploading","mib.tcp_connection_offload_state","tcpmib/TCP_CONNECTION_OFFLOAD_STATE","tcpmib/TcpConnectionOffloadStateInHost","tcpmib/TcpConnectionOffloadStateMax","tcpmib/TcpConnectionOffloadStateOffloaded","tcpmib/TcpConnectionOffloadStateOffloading","tcpmib/TcpConnectionOffloadStateUploading"]
old-location: mib\tcp_connection_offload_state.htm
tech.root: MIB
ms.assetid: cef633e7-1577-4f10-bd14-8d8e85aa78e6
ms.date: 12/05/2018
ms.keywords: '*PTCP_CONNECTION_OFFLOAD_STATE, TCP_CONNECTION_OFFLOAD_STATE, TCP_CONNECTION_OFFLOAD_STATE enumeration [MIB], TcpConnectionOffloadStateInHost, TcpConnectionOffloadStateMax, TcpConnectionOffloadStateOffloaded, TcpConnectionOffloadStateOffloading, TcpConnectionOffloadStateUploading, iprtrmib/TCP_CONNECTION_OFFLOAD_STATE, iprtrmib/TcpConnectionOffloadStateInHost, iprtrmib/TcpConnectionOffloadStateMax, iprtrmib/TcpConnectionOffloadStateOffloaded, iprtrmib/TcpConnectionOffloadStateOffloading, iprtrmib/TcpConnectionOffloadStateUploading, mib.tcp_connection_offload_state, tcpmib/TCP_CONNECTION_OFFLOAD_STATE, tcpmib/TcpConnectionOffloadStateInHost, tcpmib/TcpConnectionOffloadStateMax, tcpmib/TcpConnectionOffloadStateOffloaded, tcpmib/TcpConnectionOffloadStateOffloading, tcpmib/TcpConnectionOffloadStateUploading'
req.header: tcpmib.h
req.include-header: Iphlpapi.h
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
req.typenames: TCP_CONNECTION_OFFLOAD_STATE, *PTCP_CONNECTION_OFFLOAD_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTCP_CONNECTION_OFFLOAD_STATE
 - tcpmib/PTCP_CONNECTION_OFFLOAD_STATE
 - TCP_CONNECTION_OFFLOAD_STATE
 - tcpmib/TCP_CONNECTION_OFFLOAD_STATE
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
 - TCP_CONNECTION_OFFLOAD_STATE
---

# TCP_CONNECTION_OFFLOAD_STATE enumeration


## -description

The <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration defines the possible TCP offload states for a TCP connection.

## -enum-fields

### -field TcpConnectionOffloadStateInHost

The TCP connection is currently owned by the network stack on the local computer, and is not offloaded

### -field TcpConnectionOffloadStateOffloading

The TCP connection is in the process of being offloaded, but the offload has not been completed.

### -field TcpConnectionOffloadStateOffloaded

The TCP connection is offloaded to the network interface controller.

### -field TcpConnectionOffloadStateUploading

The TCP connection is in the process of being uploaded back to the network stack on the local computer, but the reinstate-to-host process has not completed.

### -field TcpConnectionOffloadStateMax

The maximum possible value for the <a href="/previous-versions/windows/desktop/api/tcpmib/ne-tcpmib-tcp_connection_offload_state">TCP_CONNECTION_OFFLOAD_STATE</a> enumeration type. This is not a legal value for the possible TCP connection offload state.

## -remarks

The <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration is defined on Windows Server 2003 and later. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>TCP_CONNECTION_OFFLOAD_STATE</b> enumeration  is defined in the <i>Tcpmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table2">MIB_TCP6TABLE2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow2">MIB_TCPROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable2">MIB_TCPTABLE2</a>

