---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_
title: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_
author: windows-driver-content
description: Contains information that describes an IPsec kernel drop event.
old-location: fwp\fwpm_net_event_ipsec_kernel_drop0.htm
old-project: FWP
ms.assetid: ef970199-3603-4012-9033-afa4a7301fea
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0, FWPM_NET_EVENT_IPSEC_KERNEL_DROP0 structure [Filtering], FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_, fwp.fwpm_net_event_ipsec_kernel_drop0, fwpmtypes/FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_IPSEC_KERNEL_DROP0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_IPSEC_KERNEL_DROP0_ structure


## -description


The <b>FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</b> structure contains information that describes an IPsec kernel drop event.


## -struct-fields




### -field failureStatus

Contains the  error code for the failure.


### -field direction

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552433">FWP_DIRECTION</a> value that specifies whether the dropped packet is inbound or outbound.


### -field spi

Contains the security parameters index (SPI) on the IPsec header of the packet.  This will be 0 for clear text packets.  The <b>IPSEC_SA_SPI</b> is identical to a <b>UINT32</b>.


### -field filterId

Filter ID that corresponds to the IPsec callout filter.  This will be available only if the packet was dropped by the IPsec callout.


### -field layerId

Layer ID that corresponds to the IPsec callout filter.  This will be available only if the packet was dropped by the IPsec callout.


## -remarks



<b>FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</b> is a specific implementation of FWPM_NET_EVENT_IPSEC_KERNEL_DROP. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



