---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_
title: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0 (fwpmtypes.h)
description: Contains information that describes an IPsec kernel drop event.
helpviewer_keywords: ["FWPM_NET_EVENT_IPSEC_KERNEL_DROP0","FWPM_NET_EVENT_IPSEC_KERNEL_DROP0 structure [Filtering]","fwp.fwpm_net_event_ipsec_kernel_drop0","fwpmtypes/FWPM_NET_EVENT_IPSEC_KERNEL_DROP0"]
old-location: fwp\fwpm_net_event_ipsec_kernel_drop0.htm
tech.root: fwp
ms.assetid: ef970199-3603-4012-9033-afa4a7301fea
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0, FWPM_NET_EVENT_IPSEC_KERNEL_DROP0 structure [Filtering], fwp.fwpm_net_event_ipsec_kernel_drop0, fwpmtypes/FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
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
req.typenames: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_
 - fwpmtypes/FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_
 - FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
 - fwpmtypes/FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
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
 - FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
---

# FWPM_NET_EVENT_IPSEC_KERNEL_DROP0 structure


## -description

The <b>FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</b> structure contains information that describes an IPsec kernel drop event.

## -struct-fields

### -field failureStatus

Contains the  error code for the failure.

### -field direction

An [FWP_DIRECTION](/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction) value that specifies whether the dropped packet is inbound or outbound.

### -field spi

Contains the security parameters index (SPI) on the IPsec header of the packet.  This will be 0 for clear text packets.  The <b>IPSEC_SA_SPI</b> is identical to a <b>UINT32</b>.

### -field filterId

Filter ID that corresponds to the IPsec callout filter.  This will be available only if the packet was dropped by the IPsec callout.

### -field layerId

Layer ID that corresponds to the IPsec callout filter.  This will be available only if the packet was dropped by the IPsec callout.

## -remarks

<b>FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</b> is a specific implementation of FWPM_NET_EVENT_IPSEC_KERNEL_DROP. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.