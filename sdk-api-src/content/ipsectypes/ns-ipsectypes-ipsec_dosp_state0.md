---
UID: NS:ipsectypes.IPSEC_DOSP_STATE0_
title: IPSEC_DOSP_STATE0 (ipsectypes.h)
description: Used to store state information for IPsec DoS Protection.
helpviewer_keywords: ["IPSEC_DOSP_STATE0","IPSEC_DOSP_STATE0 structure [Filtering]","fwp.ipsec_dosp_state0","ipsectypes/IPSEC_DOSP_STATE0"]
old-location: fwp\ipsec_dosp_state0.htm
tech.root: fwp
ms.assetid: e3653c19-0e0b-4026-a32d-509c4bb71008
ms.date: 12/05/2018
ms.keywords: IPSEC_DOSP_STATE0, IPSEC_DOSP_STATE0 structure [Filtering], fwp.ipsec_dosp_state0, ipsectypes/IPSEC_DOSP_STATE0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_DOSP_STATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_DOSP_STATE0_
 - ipsectypes/IPSEC_DOSP_STATE0_
 - IPSEC_DOSP_STATE0
 - ipsectypes/IPSEC_DOSP_STATE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_DOSP_STATE0
---

# IPSEC_DOSP_STATE0 structure


## -description

The <b>IPSEC_DOSP_STATE0</b> structure is used to store state information for IPsec DoS Protection.

## -struct-fields

### -field publicHostV6Addr

The IPv6 address of the public host.

### -field internalHostV6Addr

The IPv6 address of the internal host.

### -field totalInboundIPv6IPsecAuthPackets

The total number of inbound IPv6 IPsec packets that have been allowed since the state entry was created.

### -field totalOutboundIPv6IPsecAuthPackets

The total number of outbound IPv6 IPsec packets that have been allowed since the state entry was created.

### -field durationSecs

The duration, in seconds, since the state entry was created.

## -remarks

<b>IPSEC_DOSP_STATE0</b> is a specific implementation of IPSEC_DOSP_STATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>