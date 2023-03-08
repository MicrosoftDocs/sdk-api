---
UID: NS:ipsectypes.IPSEC_AGGREGATE_SA_STATISTICS0_
title: IPSEC_AGGREGATE_SA_STATISTICS0 (ipsectypes.h)
description: Stores aggregate IPsec kernel security association (SA) statistics.
helpviewer_keywords: ["IPSEC_AGGREGATE_SA_STATISTICS0","IPSEC_AGGREGATE_SA_STATISTICS0 structure [Filtering]","fwp.ipsec_aggregate_sa_statistics0_struct","ipsectypes/IPSEC_AGGREGATE_SA_STATISTICS0"]
old-location: fwp\ipsec_aggregate_sa_statistics0_struct.htm
tech.root: fwp
ms.assetid: f0318061-40f9-4380-9681-34db70659c49
ms.date: 12/05/2018
ms.keywords: IPSEC_AGGREGATE_SA_STATISTICS0, IPSEC_AGGREGATE_SA_STATISTICS0 structure [Filtering], fwp.ipsec_aggregate_sa_statistics0_struct, ipsectypes/IPSEC_AGGREGATE_SA_STATISTICS0
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
req.typenames: IPSEC_AGGREGATE_SA_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_AGGREGATE_SA_STATISTICS0_
 - ipsectypes/IPSEC_AGGREGATE_SA_STATISTICS0_
 - IPSEC_AGGREGATE_SA_STATISTICS0
 - ipsectypes/IPSEC_AGGREGATE_SA_STATISTICS0
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
 - IPSEC_AGGREGATE_SA_STATISTICS0
---

# IPSEC_AGGREGATE_SA_STATISTICS0 structure


## -description

The <b>IPSEC_AGGREGATE_SA_STATISTICS0</b> structure stores aggregate IPsec kernel security association (SA) statistics.

## -struct-fields

### -field activeSas

Number of active SAs.

### -field pendingSaNegotiations

Number of pending SA negotiations.

### -field totalSasAdded

Total number of SAs added.

### -field totalSasDeleted

Total number of SAs deleted.

### -field successfulRekeys

Number of successful re-keys.

### -field activeTunnels

Number of active tunnels.

### -field offloadedSas

Number of offloaded SAs.

## -remarks

<b>IPSEC_AGGREGATE_SA_STATISTICS0</b> is a specific implementation of IPSEC_AGGREGATE_SA_STATISTICS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>