---
UID: NS:ipsectypes.IPSEC_AH_DROP_PACKET_STATISTICS0_
title: IPSEC_AH_DROP_PACKET_STATISTICS0 (ipsectypes.h)
description: Stores IPsec AH drop packet statistics.
helpviewer_keywords: ["IPSEC_AH_DROP_PACKET_STATISTICS0","IPSEC_AH_DROP_PACKET_STATISTICS0 structure [Filtering]","fwp.ipsec_ah_drop_packet_statistics0_struct","ipsectypes/IPSEC_AH_DROP_PACKET_STATISTICS0"]
old-location: fwp\ipsec_ah_drop_packet_statistics0_struct.htm
tech.root: fwp
ms.assetid: dca4d313-fb88-475f-adee-7c42abe550d5
ms.date: 12/05/2018
ms.keywords: IPSEC_AH_DROP_PACKET_STATISTICS0, IPSEC_AH_DROP_PACKET_STATISTICS0 structure [Filtering], fwp.ipsec_ah_drop_packet_statistics0_struct, ipsectypes/IPSEC_AH_DROP_PACKET_STATISTICS0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IPSEC_AH_DROP_PACKET_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_AH_DROP_PACKET_STATISTICS0_
 - ipsectypes/IPSEC_AH_DROP_PACKET_STATISTICS0_
 - IPSEC_AH_DROP_PACKET_STATISTICS0
 - ipsectypes/IPSEC_AH_DROP_PACKET_STATISTICS0
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
 - IPSEC_AH_DROP_PACKET_STATISTICS0
---

# IPSEC_AH_DROP_PACKET_STATISTICS0 structure


## -description

The <b>IPSEC_AH_DROP_PACKET_STATISTICS0</b> structure stores IPsec AH drop packet statistics.

## -struct-fields

### -field invalidSpisOnInbound

Number of invalid SPIs on inbound.

### -field authenticationFailuresOnInbound

Number of authentication failures on inbound.

### -field replayCheckFailuresOnInbound

Number of replay check failures  on inbound.

### -field saNotInitializedOnInbound

Number of inbound drops for packets received on SAs that were not fully initialized.

## -remarks

<b>IPSEC_AH_DROP_PACKET_STATISTICS0</b> is a specific implementation of IPSEC_AH_DROP_PACKET_STATISTICS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>