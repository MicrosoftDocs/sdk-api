---
UID: NS:mprapi._PPP_INFO_3
title: PPP_INFO_3 (mprapi.h)
author: windows-sdk-content
description: The PPP_INFO_3 structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.
old-location: rras\ppp_info_3.htm
tech.root: RRAS
ms.assetid: cc231775-83bc-45d5-8bd8-7ac4cf5f09ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PPP_INFO_3, PPP_INFO_3 structure [RAS], mprapi/PPP_INFO_3, rras.ppp_info_3
ms.topic: struct
f1_keywords: ["mprapi/PPP_INFO_3"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_INFO_3
product: Windows
targetos: Windows
req.typenames: PPP_INFO_3
req.redist: 
ms.custom: 19H1
---

# PPP_INFO_3 structure


## -description


The 
<b>PPP_INFO_3</b> structure is used to report the results of the various Point-to-Point (PPP) projection operations for a connection.


## -struct-fields




### -field nbf

A 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_nbfcp_info">PPP_NBFCP_INFO</a> structure that contains PPP NetBEUI Framer (NBF) projection information.


### -field ip

A 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_ipcp_info2">PPP_IPCP_INFO2</a> structure that contains PPP Internet Protocol (IP) projection information.


### -field ipv6

A 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_ipv6_cp_info">PPP_IPV6_CP_INFO</a> structure that contains IPv6 control protocol projection information.


### -field ccp

A 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_ccp_info">PPP_CCP_INFO</a> structure that contains Compression Control Protocol (CCP) projection information.


### -field lcp

A 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_lcp_info">PPP_LCP_INFO</a> structure that contains PPP Link Control Protocol (LCP) projection information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_info">PPP_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ppp_info_2">PPP_INFO_2</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-_ras_connection_3">RAS_CONNECTION_3</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
 

 

