---
UID: NS:tdiinfo.tcp_request_query_information_ex_xp
title: TCP_REQUEST_QUERY_INFORMATION_EX_XP (tdiinfo.h)
description: The TCP_REQUEST_QUERY_INFORMATION_EX_XP structure (tdiinfo.h) contains the input for the IOCTL_TCP_QUERY_INFORMATION_EX control code.
helpviewer_keywords: ["*PTCP_REQUEST_QUERY_INFORMATION_EX","*PTCP_REQUEST_QUERY_INFORMATION_EX_XP","PTCP_REQUEST_QUERY_INFORMATION_EX","PTCP_REQUEST_QUERY_INFORMATION_EX structure pointer [Windows API]","TCP_REQUEST_QUERY_INFORMATION_EX","TCP_REQUEST_QUERY_INFORMATION_EX structure [Windows API]","TCP_REQUEST_QUERY_INFORMATION_EX_XP","tdiinfo/PTCP_REQUEST_QUERY_INFORMATION_EX","tdiinfo/TCP_REQUEST_QUERY_INFORMATION_EX","winprog.tcp_request_query_information_ex"]
old-location: winprog\tcp_request_query_information_ex.htm
tech.root: winprog
ms.assetid: 2a1f3a41-ee18-4a67-9da1-a5b18d32defb
ms.date: 08/10/2022
ms.keywords: '*PTCP_REQUEST_QUERY_INFORMATION_EX, *PTCP_REQUEST_QUERY_INFORMATION_EX_XP, PTCP_REQUEST_QUERY_INFORMATION_EX, PTCP_REQUEST_QUERY_INFORMATION_EX structure pointer [Windows API], TCP_REQUEST_QUERY_INFORMATION_EX, TCP_REQUEST_QUERY_INFORMATION_EX structure [Windows API], TCP_REQUEST_QUERY_INFORMATION_EX_XP, tdiinfo/PTCP_REQUEST_QUERY_INFORMATION_EX, tdiinfo/TCP_REQUEST_QUERY_INFORMATION_EX, winprog.tcp_request_query_information_ex'
req.header: tdiinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TCP_REQUEST_QUERY_INFORMATION_EX_XP, *PTCP_REQUEST_QUERY_INFORMATION_EX_XP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tcp_request_query_information_ex_xp
 - tdiinfo/tcp_request_query_information_ex_xp
 - PTCP_REQUEST_QUERY_INFORMATION_EX_XP
 - tdiinfo/PTCP_REQUEST_QUERY_INFORMATION_EX_XP
 - TCP_REQUEST_QUERY_INFORMATION_EX_XP
 - tdiinfo/TCP_REQUEST_QUERY_INFORMATION_EX_XP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tdiinfo.h
api_name:
 - TCP_REQUEST_QUERY_INFORMATION_EX
---

# TCP_REQUEST_QUERY_INFORMATION_EX_XP structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains the input for the <a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.

## -struct-fields

### -field ID

The <a href="/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a> structure that defines the type of information being requested from the TCP driver by <a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>.

### -field Context

The IPv4 or IPv6 address to be used when <a href="/windows/desktop/api/tcpioctl/ns-tcpioctl-ipinterfaceinfo">IPInterfaceInfo</a> data is requested for a particular IP address.

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/windows/desktop/api/tcpioctl/ns-tcpioctl-ipinterfaceinfo">IPInterfaceInfo</a>



<a href="/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a>
