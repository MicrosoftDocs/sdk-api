---
UID: NS:tcpestats._TCP_ESTATS_PATH_RW_v0
title: TCP_ESTATS_PATH_RW_v0 (tcpestats.h)
description: Contains read/write configuration information for extended TCP statistics on path measurement for a TCP connection.
helpviewer_keywords: ["*PTCP_ESTATS_PATH_RW_v0","PTCP_ESTATS_PATH_RW_v0","PTCP_ESTATS_PATH_RW_v0 structure pointer [IP Helper]","TCP_ESTATS_PATH_RW_v0","TCP_ESTATS_PATH_RW_v0 structure [IP Helper]","iphlp.tcp_estats_path_rw_v0","tcpestats/PTCP_ESTATS_PATH_RW_v0","tcpestats/TCP_ESTATS_PATH_RW_v0"]
old-location: iphlp\tcp_estats_path_rw_v0.htm
tech.root: IpHlp
ms.assetid: 460ad710-06aa-490a-9bac-5a8c731687e9
ms.date: 12/05/2018
ms.keywords: '*PTCP_ESTATS_PATH_RW_v0, PTCP_ESTATS_PATH_RW_v0, PTCP_ESTATS_PATH_RW_v0 structure pointer [IP Helper], TCP_ESTATS_PATH_RW_v0, TCP_ESTATS_PATH_RW_v0 structure [IP Helper], iphlp.tcp_estats_path_rw_v0, tcpestats/PTCP_ESTATS_PATH_RW_v0, tcpestats/TCP_ESTATS_PATH_RW_v0'
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
req.typenames: TCP_ESTATS_PATH_RW_v0, *PTCP_ESTATS_PATH_RW_v0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCP_ESTATS_PATH_RW_v0
 - tcpestats/_TCP_ESTATS_PATH_RW_v0
 - PTCP_ESTATS_PATH_RW_v0
 - tcpestats/PTCP_ESTATS_PATH_RW_v0
 - TCP_ESTATS_PATH_RW_v0
 - tcpestats/TCP_ESTATS_PATH_RW_v0
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
 - TCP_ESTATS_PATH_RW_v0
---

# TCP_ESTATS_PATH_RW_v0 structure


## -description

The <b>TCP_ESTATS_PATH_RW_v0</b> structure contains read/write configuration information for extended TCP statistics on path measurement for a TCP connection.

## -struct-fields

### -field EnableCollection

A value that indicates if extended statistics on a TCP connection should be collected for path measurement information. 

If this member is set to <b>TRUE</b>, extended statistics on the TCP connection are enabled. If this member is set to <b>FALSE</b>, extended statistics on the TCP connection are disabled. 

The default state for this member when not set is disabled.

## -remarks

The <b>TCP_ESTATS_PATH_RW_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_PATH_RW_v0</b> is defined as version 0 of the structure for  read/write configuration information on extended path measurement for a TCP connection.  This information is used to infer segment reordering on the path from the local sender to the remote receiver. 

Extended TCP statistics on extended path measurement information for a TCP connection are enabled and disabled using this structure and the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsPath</b> is passed in the <i>EstatsType</i> parameter.

The <b>TCP_ESTATS_PATH_RW_v0</b> structure is retrieved by calls to  the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsPath</b> is passed in the <i>EstatsType</i> parameter.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcp6connectionestats">GetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats">GetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcp6connectionestats">SetPerTcp6ConnectionEStats</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setpertcpconnectionestats">SetPerTcpConnectionEStats</a>



<a href="/windows/desktop/api/tcpestats/ne-tcpestats-tcp_estats_type">TCP_ESTATS_TYPE</a>