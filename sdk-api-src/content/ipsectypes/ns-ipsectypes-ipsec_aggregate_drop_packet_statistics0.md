---
UID: NS:ipsectypes.IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0_
title: IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0 (ipsectypes.h)
description: Stores aggregate IPsec kernel packet drop statistics.Note  IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0 is the specific implementation of IPSEC_AGGREGATE_DROP_PACKET_STATISTICS used in Windows Vista.
helpviewer_keywords: ["IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0","IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0 structure [Filtering]","fwp.ipsec_aggregate_drop_packet_statistics0_struct","ipsectypes/IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0"]
old-location: fwp\ipsec_aggregate_drop_packet_statistics0_struct.htm
tech.root: fwp
ms.assetid: f7c955af-97ec-4c27-a9de-d1498398608e
ms.date: 12/05/2018
ms.keywords: IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0, IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0 structure [Filtering], fwp.ipsec_aggregate_drop_packet_statistics0_struct, ipsectypes/IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0
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
req.typenames: IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0_
 - ipsectypes/IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0_
 - IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0
 - ipsectypes/IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0
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
 - IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0
---

# IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0 structure


## -description

The [IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) is available.</div>
<div> </div>

## -struct-fields

### -field invalidSpisOnInbound

Number of invalid SPIs on inbound.

### -field decryptionFailuresOnInbound

Number of decryption failures on inbound.

### -field authenticationFailuresOnInbound

Number of authentication failures on inbound.

### -field udpEspValidationFailuresOnInbound

Number of UDP ESP validation failures on inbound.

### -field replayCheckFailuresOnInbound

Number of replay check failures on inbound.

### -field invalidClearTextInbound

Number of invalid clear text instances on inbound.

### -field saNotInitializedOnInbound

Number of inbound drops for packets received on SAs that were not fully initialized.

### -field receiveOverIncorrectSaInbound

Number of inbound drops for packets received on SAs whose characteristics did not match the packet.

### -field secureReceivesNotMatchingFilters

Number of inbound IPsec secured packets that did not match any inbound IPsec transport layer filter.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>