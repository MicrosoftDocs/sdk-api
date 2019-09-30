---
UID: NS:tdiinfo.tcp_request_query_information_ex_w2k
title: TCP_REQUEST_QUERY_INFORMATION_EX_W2K (tdiinfo.h)
author: windows-sdk-content
description: Contains the input for the IOCTL_TCP_QUERY_INFORMATION_EX control code.
old-location: winprog\tcp_request_query_information_ex.htm
tech.root: DevNotes
ms.assetid: 2a1f3a41-ee18-4a67-9da1-a5b18d32defb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTCP_REQUEST_QUERY_INFORMATION_EX, *PTCP_REQUEST_QUERY_INFORMATION_EX_W2K, PTCP_REQUEST_QUERY_INFORMATION_EX, PTCP_REQUEST_QUERY_INFORMATION_EX structure pointer [Windows API], TCP_REQUEST_QUERY_INFORMATION_EX, TCP_REQUEST_QUERY_INFORMATION_EX structure [Windows API], TCP_REQUEST_QUERY_INFORMATION_EX_W2K, tdiinfo/PTCP_REQUEST_QUERY_INFORMATION_EX, tdiinfo/TCP_REQUEST_QUERY_INFORMATION_EX, winprog.tcp_request_query_information_ex"
ms.topic: struct
f1_keywords: 
 - "tdiinfo/TCP_REQUEST_QUERY_INFORMATION_EX"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tdiinfo.h
api_name:
 - TCP_REQUEST_QUERY_INFORMATION_EX
targetos: Windows
req.typenames: TCP_REQUEST_QUERY_INFORMATION_EX_W2K, *PTCP_REQUEST_QUERY_INFORMATION_EX_W2K
req.redist: 
ms.custom: 19H1
---

# TCP_REQUEST_QUERY_INFORMATION_EX_W2K structure


## -description


<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains the input for the <a href="https://docs.microsoft.com/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.


## -struct-fields




### -field ID

The <a href="https://docs.microsoft.com/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a> structure that defines the type of information being requested from the TCP driver by <a href="https://docs.microsoft.com/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>.


### -field Context

The IPv4 or IPv6 address to be used when <a href="https://docs.microsoft.com/windows/desktop/api/tcpioctl/ns-tcpioctl-ipinterfaceinfo">IPInterfaceInfo</a> data is requested for a particular IP address.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tcpioctl/ns-tcpioctl-ipinterfaceinfo">IPInterfaceInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a>
 

 

