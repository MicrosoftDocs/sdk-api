---
UID: NS:mprapi._PPP_IPXCP_INFO
title: PPP_IPXCP_INFO (mprapi.h)
description: The PPP_IPXCP_INFO structure contains the result of a PPP Internetwork Packet Exchange (IPX) projection operation.
helpviewer_keywords: ["PPP_IPXCP_INFO","PPP_IPXCP_INFO structure [RAS]","_mpr_ppp_ipxcp_info","mprapi/PPP_IPXCP_INFO","rras.ppp_ipxcp_info"]
old-location: rras\ppp_ipxcp_info.htm
tech.root: RRAS
ms.assetid: 6e269c4e-8014-4d59-a7dc-3314a67a4d12
ms.date: 12/05/2018
ms.keywords: PPP_IPXCP_INFO, PPP_IPXCP_INFO structure [RAS], _mpr_ppp_ipxcp_info, mprapi/PPP_IPXCP_INFO, rras.ppp_ipxcp_info
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
req.typenames: PPP_IPXCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_IPXCP_INFO
 - mprapi/_PPP_IPXCP_INFO
 - PPP_IPXCP_INFO
 - mprapi/PPP_IPXCP_INFO
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
 - PPP_IPXCP_INFO
---

# PPP_IPXCP_INFO structure


## -description

The 
<b>PPP_IPXCP_INFO</b> structure contains the result of a PPP Internetwork Packet Exchange (IPX) projection operation.

## -struct-fields

### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.

### -field wszAddress

Specifies a Unicode string that holds the client's IPX address on the RAS connection. This address string has the form <i>net</i><b>.</b><i>node</i>, for example, "1234ABCD.12AB34CD56EF".

## -remarks

The 
<b>PPP_IPXCP_INFO</b> structure can be used only when administrating computers that are running 32-bit Windows Server 2003 or an earlier operating system. Windows 2000 64-bit Edition does not support the IPX protocol.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>