---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP0_
title: FWPM_NET_EVENT_CLASSIFY_DROP0 (fwpmtypes.h)
description: Contains information that describes a layer drop failure. (FWPM_NET_EVENT_CLASSIFY_DROP0)
helpviewer_keywords: ["FWPM_NET_EVENT_CLASSIFY_DROP0","FWPM_NET_EVENT_CLASSIFY_DROP0 structure [Filtering]","fwp.fwpm_net_event_classify_drop0","fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0"]
old-location: fwp\fwpm_net_event_classify_drop0.htm
tech.root: fwp
ms.assetid: 9688ff75-292f-44f2-b3ed-41a9dd1ef918
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP0, FWPM_NET_EVENT_CLASSIFY_DROP0 structure [Filtering], fwp.fwpm_net_event_classify_drop0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CLASSIFY_DROP0_
 - fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0_
 - FWPM_NET_EVENT_CLASSIFY_DROP0
 - fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_CLASSIFY_DROP0
---

# FWPM_NET_EVENT_CLASSIFY_DROP0 structure


## -description

The **FWPM_NET_EVENT_CLASSIFY_DROP0** structure contains information that describes a layer drop  failure.
[FWPM_NET_EVENT_CLASSIFY_DROP1](ns-fwpmtypes-fwpm_net_event_classify_drop1.md) is available. For Windows 8, [FWPM_NET_EVENT_CLASSIFY_DROP2](ns-fwpmtypes-fwpm_net_event_classify_drop2.md) is available.

## -struct-fields

### -field filterId

A LUID identifying the filter where the failure occurred.

### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see [Filtering Layer Identifiers](/windows/desktop/FWP/management-filtering-layer-identifiers-).

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
