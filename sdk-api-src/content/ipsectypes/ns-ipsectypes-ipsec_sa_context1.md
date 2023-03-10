---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT1_
title: IPSEC_SA_CONTEXT1 (ipsectypes.h)
description: Encapsulates an inbound and outbound security association (SA) pair.
helpviewer_keywords: ["IPSEC_SA_CONTEXT1","IPSEC_SA_CONTEXT1 structure [Filtering]","fwp.ipsec_sa_context1","ipsectypes/IPSEC_SA_CONTEXT1"]
old-location: fwp\ipsec_sa_context1.htm
tech.root: fwp
ms.assetid: a3e210a7-cd3a-42fc-b3a0-7df9ad6778af
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT1, IPSEC_SA_CONTEXT1 structure [Filtering], fwp.ipsec_sa_context1, ipsectypes/IPSEC_SA_CONTEXT1
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
req.typenames: IPSEC_SA_CONTEXT1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_CONTEXT1_
 - ipsectypes/IPSEC_SA_CONTEXT1_
 - IPSEC_SA_CONTEXT1
 - ipsectypes/IPSEC_SA_CONTEXT1
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
 - IPSEC_SA_CONTEXT1
---

# IPSEC_SA_CONTEXT1 structure


## -description

The <b>IPSEC_SA_CONTEXT1</b> structure encapsulates an inbound and outbound security association (SA) pair.
[IPSEC_SA_CONTEXT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context0) is available.</div><div> </div>

## -struct-fields

### -field saContextId

Identifies the SA context.

### -field inboundSa

An [IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1) structure that contains information about the inbound SA.

### -field outboundSa

An [IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1) structure that contains information about the outbound SA.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>