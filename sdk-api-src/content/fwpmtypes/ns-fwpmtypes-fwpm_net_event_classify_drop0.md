---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP0_
title: FWPM_NET_EVENT_CLASSIFY_DROP0 (fwpmtypes.h)
description: Contains information that describes a layer drop failure.
old-location: fwp\fwpm_net_event_classify_drop0.htm
tech.root: fwp
ms.assetid: 9688ff75-292f-44f2-b3ed-41a9dd1ef918
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP0, FWPM_NET_EVENT_CLASSIFY_DROP0 structure [Filtering], fwp.fwpm_net_event_classify_drop0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0
ms.topic: struct
f1_keywords:
- fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP0
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_NET_EVENT_CLASSIFY_DROP0
targetos: Windows
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP0
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_CLASSIFY_DROP0 structure


## -description


The <b>FWPM_NET_EVENT_CLASSIFY_DROP0</b> structure contains information that describes a layer drop  failure.
[FWPM_NET_EVENT_CLASSIFY_DROP1](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1)a> is available. For Windows 8, [FWPM_NET_EVENT_CLASSIFY_DROP2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)a> is available. </div><div> </div>

## -struct-fields




### -field filterId

A LUID identifying the filter where the failure occurred.


### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see <a href="https://docs.microsoft.com/windows/desktop/FWP/management-filtering-layer-identifiers-">Filtering Layer Identifiers</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

