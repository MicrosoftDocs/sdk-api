---
UID: NS:fwpmtypes.FWPM_STATISTICS0_
title: FWPM_STATISTICS0 (fwpmtypes.h)
description: Stores statistics related to connections at specific layers.
helpviewer_keywords: ["FWPM_STATISTICS0","FWPM_STATISTICS0 structure [Filtering]","fwp.fwpm_statistics0","fwpmtypes/FWPM_STATISTICS0"]
old-location: fwp\fwpm_statistics0.htm
tech.root: fwp
ms.assetid: c3ac6871-79b1-4378-8f3c-a56e85fd2a3b
ms.date: 12/05/2018
ms.keywords: FWPM_STATISTICS0, FWPM_STATISTICS0 structure [Filtering], fwp.fwpm_statistics0, fwpmtypes/FWPM_STATISTICS0
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
req.typenames: FWPM_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_STATISTICS0_
 - fwpmtypes/FWPM_STATISTICS0_
 - FWPM_STATISTICS0
 - fwpmtypes/FWPM_STATISTICS0
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
 - FWPM_STATISTICS0
---

# FWPM_STATISTICS0 structure


## -description

The <b>FWPM_STATISTICS0</b> structure stores statistics related to connections at specific layers.

## -struct-fields

### -field numLayerStatistics

Type: <b>UINT32</b>

Number of [FWPM_LAYER_STATISTICS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0) structures in the <b>layerStatistics</b> member.

### -field layerStatistics

Type: [FWPM_LAYER_STATISTICS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)*</b>

Statistics related to the layer.

### -field inboundAllowedConnectionsV4

Type: <b>UINT32</b>

Number of allowed IPv4 inbound connections.

### -field inboundBlockedConnectionsV4

Type: <b>UINT32</b>

Number of blocked IPv4 inbound connections.

### -field outboundAllowedConnectionsV4

Type: <b>UINT32</b>

Number of allowed IPv4 outbound connections.

### -field outboundBlockedConnectionsV4

Type: <b>UINT32</b>

Number of blocked IPv4 outbound connections.

### -field inboundAllowedConnectionsV6

Type: <b>UINT32</b>

Number of allowed IPv6 inbound connections.

### -field inboundBlockedConnectionsV6

Type: <b>UINT32</b>

Number of blocked IPv6 inbound connections.

### -field outboundAllowedConnectionsV6

Type: <b>UINT32</b>

Number of allowed IPv6 outbound connections.

### -field outboundBlockedConnectionsV6

Type: <b>UINT32</b>

Number of blocked IPv6 outbound connections.

### -field inboundActiveConnectionsV4

Type: <b>UINT32</b>

Number of active IPv4 inbound connections.

### -field outboundActiveConnectionsV4

Type: <b>UINT32</b>

Number of active IPv4 outbound connections.

### -field inboundActiveConnectionsV6

Type: <b>UINT32</b>

Number of active IPv6 inbound connections.

### -field outboundActiveConnectionsV6

Type: <b>UINT32</b>

Number of active IPv6 outbound connections.

### -field reauthDirInbound

### -field reauthDirOutbound

### -field reauthFamilyV4

### -field reauthFamilyV6

### -field reauthProtoOther

### -field reauthProtoIPv4

### -field reauthProtoIPv6

### -field reauthProtoICMP

### -field reauthProtoICMP6

### -field reauthProtoUDP

### -field reauthProtoTCP

### -field reauthReasonPolicyChange

### -field reauthReasonNewArrivalInterface

### -field reauthReasonNewNextHopInterface

### -field reauthReasonProfileCrossing

### -field reauthReasonClassifyCompletion

### -field reauthReasonIPSecPropertiesChanged

### -field reauthReasonMidStreamInspection

### -field reauthReasonSocketPropertyChanged

### -field reauthReasonNewInboundMCastBCastPacket

### -field reauthReasonEDPPolicyChanged

### -field reauthReasonPreclassifyLocalAddrLayerChange

### -field reauthReasonPreclassifyRemoteAddrLayerChange

### -field reauthReasonPreclassifyLocalPortLayerChange

### -field reauthReasonPreclassifyRemotePortLayerChange

### -field reauthReasonProxyHandleChanged

## -remarks

<b>FWPM_STATISTICS0</b> is a specific implementation of FWPM_STATISTICS. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_LAYER_STATISTICS0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)