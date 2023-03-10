---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_ALLOW0
title: FWPM_NET_EVENT_CLASSIFY_ALLOW0 (fwpmtypes.h)
description: Contains information that describes allowed traffic as enforced by the WFP classify engine.
helpviewer_keywords: ["FWPM_NET_EVENT_CLASSIFY_ALLOW0","FWPM_NET_EVENT_CLASSIFY_ALLOW0 structure [Filtering]","fwp.fwpm_net_event_classify_allow0","fwpmtypes/FWPM_NET_EVENT_CLASSIFY_ALLOW0"]
old-location: fwp\fwpm_net_event_classify_allow0.htm
tech.root: fwp
ms.assetid: 4c7b665e-b248-4506-8d5f-bd27b05d8d50
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_ALLOW0, FWPM_NET_EVENT_CLASSIFY_ALLOW0 structure [Filtering], fwp.fwpm_net_event_classify_allow0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_ALLOW0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT_CLASSIFY_ALLOW0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CLASSIFY_ALLOW0
 - fwpmtypes/FWPM_NET_EVENT_CLASSIFY_ALLOW0
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
 - FWPM_NET_EVENT_CLASSIFY_ALLOW0
---

# FWPM_NET_EVENT_CLASSIFY_ALLOW0 structure


## -description

The <b>FWPM_NET_EVENT_CLASSIFY_ALLOW0</b> structure contains information that describes allowed traffic as enforced by the WFP classify engine.

## -struct-fields

### -field filterId

Type: <b>UINT64</b>

A LUID identifying the WFP filter allowing this traffic.

### -field layerId

Type: <b>UINT16</b>

The identifier of the WFP filtering layer where the filter specified  in <b>filterId</b> is stored. For more information, see <a href="/windows/desktop/FWP/management-filtering-layer-identifiers-">Filtering Layer Identifiers</a>.

### -field reauthReason

Type: <b>UINT32</b>

The reason for reauthorizing a previously authorized connection.

### -field originalProfile

Type: <b>UINT32</b>

The identifier of the profile to which the packet was received (or from which the packet was sent).

### -field currentProfile

Type: <b>UINT32</b>

The identifier of the profile where the packet was when the failure occurred.

### -field msFwpDirection

Type: <b>UINT32</b>

Indicates the direction of the packet transmission. Possible values are <b>FWP_DIRECTION_INBOUND</b> or <b>FWP_DIRECTION_OUTBOUND</b>.

### -field isLoopback

Type: <b>BOOL</b>

If true, indicates that the packet originated from (or was heading to) the loopback adapter; otherwise, false.

## -see-also

[FWPM_NET_EVENT2](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event2)