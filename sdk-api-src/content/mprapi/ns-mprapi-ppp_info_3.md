---
UID: NS:mprapi._PPP_INFO_3
title: PPP_INFO_3 (mprapi.h)
description: The PPP_INFO_3 structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.
helpviewer_keywords: ["PPP_INFO_3","PPP_INFO_3 structure [RAS]","mprapi/PPP_INFO_3","rras.ppp_info_3"]
old-location: rras\ppp_info_3.htm
tech.root: RRAS
ms.assetid: cc231775-83bc-45d5-8bd8-7ac4cf5f09ff
ms.date: 12/05/2018
ms.keywords: PPP_INFO_3, PPP_INFO_3 structure [RAS], mprapi/PPP_INFO_3, rras.ppp_info_3
req.header: mprapi.h
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
req.typenames: PPP_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_INFO_3
 - mprapi/_PPP_INFO_3
 - PPP_INFO_3
 - mprapi/PPP_INFO_3
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
 - PPP_INFO_3
---

# PPP_INFO_3 structure


## -description

The 
<b>PPP_INFO_3</b> structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.

## -struct-fields

### -field nbf

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_nbfcp_info">PPP_NBFCP_INFO</a> structure that contains PPP NetBEUI Framer (NBF) projection information.

### -field ip

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ipcp_info2">PPP_IPCP_INFO2</a> structure that contains PPP Internet Protocol (IP) projection information.

### -field ipv6

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ipv6_cp_info">PPP_IPV6_CP_INFO</a> structure that contains IPv6 control protocol projection information.

### -field ccp

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ccp_info">PPP_CCP_INFO</a> structure that contains Compression Control Protocol (CCP) projection information.

### -field lcp

A 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_lcp_info">PPP_LCP_INFO</a> structure that contains PPP Link Control Protocol (LCP) projection information.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info_2">PPP_INFO_2</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>