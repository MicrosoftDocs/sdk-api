---
UID: NS:ipsectypes.IPSEC_SA_LIFETIME0_
title: IPSEC_SA_LIFETIME0 (ipsectypes.h)
description: Stores the lifetime in seconds/kilobytes/packets for an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_SA_LIFETIME0","IPSEC_SA_LIFETIME0 structure [Filtering]","fwp.ipsec_sa_lifetime0_struct","ipsectypes/IPSEC_SA_LIFETIME0"]
old-location: fwp\ipsec_sa_lifetime0_struct.htm
tech.root: fwp
ms.assetid: 9ade5a9a-5c48-4a94-bb35-77f9866e8e6f
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_LIFETIME0, IPSEC_SA_LIFETIME0 structure [Filtering], fwp.ipsec_sa_lifetime0_struct, ipsectypes/IPSEC_SA_LIFETIME0
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
req.typenames: IPSEC_SA_LIFETIME0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_LIFETIME0_
 - ipsectypes/IPSEC_SA_LIFETIME0_
 - IPSEC_SA_LIFETIME0
 - ipsectypes/IPSEC_SA_LIFETIME0
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
 - IPSEC_SA_LIFETIME0
---

# IPSEC_SA_LIFETIME0 structure


## -description

The <b>IPSEC_SA_LIFETIME0</b> structure stores the lifetime in seconds/kilobytes/packets for an IPsec security association (SA).

## -struct-fields

### -field lifetimeSeconds

SA lifetime in seconds.

### -field lifetimeKilobytes

SA lifetime in kilobytes.

### -field lifetimePackets

SA lifetime in packets.

## -remarks

<b>IPSEC_SA_LIFETIME0</b> is a specific implementation of IPSEC_SA_LIFETIME. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>