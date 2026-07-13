---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP2_
title: FWPM_NET_EVENT_CLASSIFY_DROP2 (fwpmtypes.h)
description: Contains information that describes a layer drop failure. (FWPM_NET_EVENT_CLASSIFY_DROP2)
helpviewer_keywords: ["FWPM_NET_EVENT_CLASSIFY_DROP2","FWPM_NET_EVENT_CLASSIFY_DROP2 structure [Filtering]","FWP_DIRECTION_FORWARD","FWP_DIRECTION_IN","FWP_DIRECTION_OUT","fwp.fwpm_net_event_classify_drop2","fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP2"]
old-location: fwp\fwpm_net_event_classify_drop2.htm
tech.root: fwp
ms.assetid: 1e018d6c-ed56-43f9-90b3-f2af42861617
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP2, FWPM_NET_EVENT_CLASSIFY_DROP2 structure [Filtering], FWP_DIRECTION_FORWARD, FWP_DIRECTION_IN, FWP_DIRECTION_OUT, fwp.fwpm_net_event_classify_drop2, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP2
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwmptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_CLASSIFY_DROP2_
 - fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP2_
 - FWPM_NET_EVENT_CLASSIFY_DROP2
 - fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_CLASSIFY_DROP2
---

# FWPM_NET_EVENT_CLASSIFY_DROP2 structure


## -description

The **FWPM_NET_EVENT_CLASSIFY_DROP2** structure contains information that describes a layer drop  failure.
[FWPM_NET_EVENT_CLASSIFY_DROP1](ns-fwpmtypes-fwpm_net_event_classify_drop1.md) is available. For Windows Vista, [FWPM_NET_EVENT_CLASSIFY_DROP0](ns-fwpmtypes-fwpm_net_event_classify_drop0.md) is available.

## -struct-fields

### -field filterId

A LUID identifying the filter where the failure occurred.

### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see [Filtering Layer Identifiers](/windows/desktop/FWP/management-filtering-layer-identifiers-).

### -field reauthReason

Indicates the reason for reauthorizing a previously authorized connection.

### -field originalProfile

Indicates the identifier of the profile to which  the  packet was received (or from which the packet was sent).

### -field currentProfile

Indicates the identifier of the profile where the packet was when the failure occurred.

### -field msFwpDirection

Indicates the direction of the packet transmission.

Possible values:

| Value | Meaning |
| ----- | ------- |
| FWP_DIRECTION_IN <br/> 0x00003900L | The packet is inbound. |
| FWP_DIRECTION_OUT <br/> 0x00003901L | The packet is outbound. |
| FWP_DIRECTION_FORWARD <br/> 0x00003902L | The packet is traversing an interface which it must pass through on the way to its destination. |

### -field isLoopback

Indicates whether the packet originated from (or was heading to) the loopback adapter.

### -field vSwitchId

GUID identifier of a vSwitch.

### -field vSwitchSourcePort

Transient source port of a packet within the vSwitch.

### -field vSwitchDestinationPort

Transient destination port of a packet within the vSwitch.

## -see-also

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)
