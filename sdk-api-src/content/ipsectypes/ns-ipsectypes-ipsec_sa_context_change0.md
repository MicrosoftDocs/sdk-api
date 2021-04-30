---
UID: NS:ipsectypes.IPSEC_SA_CONTEXT_CHANGE0_
title: IPSEC_SA_CONTEXT_CHANGE0 (ipsectypes.h)
description: Contains information about an IPsec security association (SA) context change.
helpviewer_keywords: ["IPSEC_SA_CONTEXT_CHANGE0","IPSEC_SA_CONTEXT_CHANGE0 structure [Filtering]","fwp.ipsec_sa_context_change0","ipsectypes/IPSEC_SA_CONTEXT_CHANGE0"]
old-location: fwp\ipsec_sa_context_change0.htm
tech.root: fwp
ms.assetid: a81df783-72d8-4374-a3f8-44c3491a98db
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CONTEXT_CHANGE0, IPSEC_SA_CONTEXT_CHANGE0 structure [Filtering], fwp.ipsec_sa_context_change0, ipsectypes/IPSEC_SA_CONTEXT_CHANGE0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IPSEC_SA_CONTEXT_CHANGE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_CONTEXT_CHANGE0_
 - ipsectypes/IPSEC_SA_CONTEXT_CHANGE0_
 - IPSEC_SA_CONTEXT_CHANGE0
 - ipsectypes/IPSEC_SA_CONTEXT_CHANGE0
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
 - IPSEC_SA_CONTEXT_CHANGE0
---

# IPSEC_SA_CONTEXT_CHANGE0 structure


## -description

The <b>IPSEC_SA_CONTEXT_CHANGE0</b> structure contains information about an IPsec security association (SA) context  change.

## -struct-fields

### -field changeType

Type: [IPSEC_SA_CONTEXT_EVENT_TYPE0](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)</b>

The type of IPsec SA context change event.

### -field saContextId

Type: <b>UINT64</b>

Identifier of the IPsec SA context that changed.

## -see-also

[IPSEC_SA_CONTEXT_EVENT_TYPE0](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)