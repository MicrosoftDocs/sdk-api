---
UID: NS:mprapi._PPP_IPV6_CP_INFO
title: PPP_IPV6_CP_INFO (mprapi.h)
description: Contains the result of an IPv6 control protocol negotiation.
helpviewer_keywords: ["PPPP_IPV6_CP_INFO","PPPP_IPV6_CP_INFO structure pointer [RAS]","PPP_IPV6_CP_INFO","PPP_IPV6_CP_INFO structure [RAS]","mprapi/PPPP_IPV6_CP_INFO","mprapi/PPP_IPV6_CP_INFO","rras.ppp_ipv6cp_info"]
old-location: rras\ppp_ipv6cp_info.htm
tech.root: RRAS
ms.assetid: fb77a15d-a513-456d-9d55-258b93fe8db5
ms.date: 12/05/2018
ms.keywords: PPPP_IPV6_CP_INFO, PPPP_IPV6_CP_INFO structure pointer [RAS], PPP_IPV6_CP_INFO, PPP_IPV6_CP_INFO structure [RAS], mprapi/PPPP_IPV6_CP_INFO, mprapi/PPP_IPV6_CP_INFO, rras.ppp_ipv6cp_info
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
req.typenames: PPP_IPV6_CP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_IPV6_CP_INFO
 - mprapi/_PPP_IPV6_CP_INFO
 - PPP_IPV6_CP_INFO
 - mprapi/PPP_IPV6_CP_INFO
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
 - PPP_IPV6_CP_INFO
---

# PPP_IPV6_CP_INFO structure


## -description

The <b>PPP_IPV6_CP_INFO</b> structure contains the result of an IPv6 control protocol negotiation.

## -struct-fields

### -field dwVersion

The version of the <b>PPP_IPV6_CP_INFO</b> structure used.

### -field dwSize

The size, in bytes, of this <b>PPP_IPV6_CP_INFO</b> structure.

### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.

### -field bInterfaceIdentifier

Specifies the 64 bit interface identifier of the IPv6 server interface.

### -field bRemoteInterfaceIdentifier

Specifies the 64 bit interface identifier of the IPv6 client interface.

### -field dwOptions

Reserved. Must be set to 0.

### -field dwRemoteOptions

Reserved. Must be set to 0.

### -field bPrefix

Specifies the address prefix of the IPv6 client interface.

### -field dwPrefixLength

The length, in bits, of the address prefix.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>