---
UID: NS:mprapi._PPP_IPCP_INFO
title: PPP_IPCP_INFO (mprapi.h)
description: The PPP_IPCP_INFO structure contains the result of a PPP Internet Protocol (IP) negotiation.
helpviewer_keywords: ["PPP_IPCP_INFO","PPP_IPCP_INFO structure [RAS]","_mpr_ppp_ipcp_info","mprapi/PPP_IPCP_INFO","rras.ppp_ipcp_info"]
old-location: rras\ppp_ipcp_info.htm
tech.root: RRAS
ms.assetid: c77f54d2-eac4-4e0a-92c5-c46d521a272d
ms.date: 12/05/2018
ms.keywords: PPP_IPCP_INFO, PPP_IPCP_INFO structure [RAS], _mpr_ppp_ipcp_info, mprapi/PPP_IPCP_INFO, rras.ppp_ipcp_info
req.header: mprapi.h
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
req.typenames: PPP_IPCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_IPCP_INFO
 - mprapi/_PPP_IPCP_INFO
 - PPP_IPCP_INFO
 - mprapi/PPP_IPCP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_IPCP_INFO
---

# PPP_IPCP_INFO structure


## -description

The 
<b>PPP_IPCP_INFO</b> structure contains the result of a PPP Internet Protocol (IP) negotiation.

## -struct-fields

### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.

### -field wszAddress

Specifies a Unicode string that holds the local computer's IP address for the connection. This string has the form <i>a</i><b>.</b><i>b</i><b>.</b><i>c</i><b>.</b><i>d</i>; for example, "10.102.235.84". 




The 
<b>PPP_IPCP_INFO</b> structures provides address information from the perspective of the server. For example, if a remote access client is connecting to a RAS server, this member holds the IP address of the server.

### -field wszRemoteAddress

Specifies a Unicode string that holds the IP address of the remote computer. This string has the form <i>a</i><b>.</b><i>b</i><b>.</b><i>c</i><b>.</b><i>d</i>. If the address is not available, this member is an empty string. 




The 
<b>PPP_IPCP_INFO</b> structures provides address information from the perspective of the server. For example, if a remote access client is connecting to a RAS server, this member holds the IP address of the client.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ipcp_info2">PPP_IPCP_INFO2</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>