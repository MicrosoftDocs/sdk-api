---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IPSEC_DOSP_DROP0_
title: FWPM_NET_EVENT_IPSEC_DOSP_DROP0 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information that describes an IPsec DoS Protection drop event.
old-location: fwp\fwpm_net_event_ipsec_dosp_drop0.htm
tech.root: fwp
ms.assetid: 7b28a81f-bf80-4739-989e-a276a0ca8a3a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_IPSEC_DOSP_DROP0, FWPM_NET_EVENT_IPSEC_DOSP_DROP0 structure [Filtering], fwp.fwpm_net_event_ipsec_dosp_drop0, fwpmtypes/FWPM_NET_EVENT_IPSEC_DOSP_DROP0
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - FWPM_NET_EVENT_IPSEC_DOSP_DROP0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_IPSEC_DOSP_DROP0
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_IPSEC_DOSP_DROP0 structure


## -description


The <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP0</b> structure contains information that describes an IPsec DoS Protection drop event.


## -struct-fields




### -field ipVersion

Internet Protocol (IP) version.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a> for more information.


### -field publicHostV4Addr

The public IPv4 address of the Internet host.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field publicHostV6Addr

The public IPv6 address of the Internet host.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field internalHostV4Addr

The internal IPv4 address of the Internet host.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field internalHostV6Addr

The internal IPv6 address of the Internet host.

Specified when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field failureStatus

Contains the  error code for the failure.


### -field direction

An <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction_">FWP_DIRECTION</a> value that specifies whether the dropped packet is inbound or outbound.


## -remarks



<b>FWPM_NET_EVENT_IPSEC_DOSP_DROP0</b> is a specific implementation of FWPM_NET_EVENT_IPSEC_DOSP_DROP. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_direction_">FWP_DIRECTION</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

