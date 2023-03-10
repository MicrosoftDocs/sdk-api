---
UID: NS:ipsectypes.IPSEC_TRAFFIC_STATISTICS0_
title: IPSEC_TRAFFIC_STATISTICS0 (ipsectypes.h)
description: Stores IPsec traffic statistics. (IPSEC_TRAFFIC_STATISTICS0)
helpviewer_keywords: ["IPSEC_TRAFFIC_STATISTICS0","IPSEC_TRAFFIC_STATISTICS0 structure [Filtering]","fwp.ipsec_traffic_statistics0_struct","ipsectypes/IPSEC_TRAFFIC_STATISTICS0"]
old-location: fwp\ipsec_traffic_statistics0_struct.htm
tech.root: fwp
ms.assetid: 70f67966-0ced-49a7-9d27-6976ee0bd89c
ms.date: 12/05/2018
ms.keywords: IPSEC_TRAFFIC_STATISTICS0, IPSEC_TRAFFIC_STATISTICS0 structure [Filtering], fwp.ipsec_traffic_statistics0_struct, ipsectypes/IPSEC_TRAFFIC_STATISTICS0
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
req.typenames: IPSEC_TRAFFIC_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_TRAFFIC_STATISTICS0_
 - ipsectypes/IPSEC_TRAFFIC_STATISTICS0_
 - IPSEC_TRAFFIC_STATISTICS0
 - ipsectypes/IPSEC_TRAFFIC_STATISTICS0
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
 - IPSEC_TRAFFIC_STATISTICS0
---

# IPSEC_TRAFFIC_STATISTICS0 structure


## -description

The <b>IPSEC_TRAFFIC_STATISTICS0</b> structure stores IPsec traffic statistics.
[IPSEC_TRAFFIC_STATISTICS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) is available.</div><div> </div>

## -struct-fields

### -field encryptedByteCount

Specifies encrypted byte count.

### -field authenticatedAHByteCount

Specifies authenticated AH byte count.

### -field authenticatedESPByteCount

Specifies authenticated ESP byte count.

### -field transportByteCount

Specifies transport byte count.

### -field tunnelByteCount

Specifies tunnel byte count.

### -field offloadByteCount

Specifies offload byte count.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
