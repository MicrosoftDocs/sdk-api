---
UID: NS:mprapi._PPP_INFO
title: PPP_INFO (mprapi.h)
description: The PPP_INFO structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.
helpviewer_keywords: ["PPP_INFO","PPP_INFO structure [RAS]","_mpr_ppp_info","mprapi/PPP_INFO","rras.ppp_info"]
old-location: rras\ppp_info.htm
tech.root: RRAS
ms.assetid: 39692a38-ab40-43da-a704-8c206be72ceb
ms.date: 12/05/2018
ms.keywords: PPP_INFO, PPP_INFO structure [RAS], _mpr_ppp_info, mprapi/PPP_INFO, rras.ppp_info
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
req.typenames: PPP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_INFO
 - mprapi/_PPP_INFO
 - PPP_INFO
 - mprapi/PPP_INFO
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
 - PPP_INFO
---

# PPP_INFO structure


## -description

The 
<b>PPP_INFO</b> structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.

## -struct-fields

### -field nbf

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_nbfcp_info">PPP_NBFCP_INFO</a> structure that contains PPP NetBEUI Framer (NBF) projection information.

### -field ip

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ipcp_info">PPP_IPCP_INFO</a> structure that contains PPP Internet Protocol (IP) projection information.

### -field ipx

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ipxcp_info">PPP_IPXCP_INFO</a> structure that contains PPP Internetwork Packet Exchange (IPX) projection information.

### -field at

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_atcp_info">PPP_ATCP_INFO</a> structure that contains PPP AppleTalk projection information.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info_2">PPP_INFO_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info_3">PPP_INFO_3</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>