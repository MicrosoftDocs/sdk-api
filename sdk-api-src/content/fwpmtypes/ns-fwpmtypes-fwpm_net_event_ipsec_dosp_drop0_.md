---
UID: NS:fwpmtypes.FWPM_NET_EVENT_IPSEC_DOSP_DROP0_
title: FWPM_NET_EVENT_IPSEC_DOSP_DROP0_
author: windows-sdk-content
description: Contains information that describes an IPsec DoS Protection drop event.
old-location: fwp\fwpm_net_event_ipsec_dosp_drop0.htm
old-project: FWP
ms.assetid: 7b28a81f-bf80-4739-989e-a276a0ca8a3a
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FWPM_NET_EVENT_IPSEC_DOSP_DROP0, FWPM_NET_EVENT_IPSEC_DOSP_DROP0 structure [Filtering], FWPM_NET_EVENT_IPSEC_DOSP_DROP0_, fwp.fwpm_net_event_ipsec_dosp_drop0, fwpmtypes/FWPM_NET_EVENT_IPSEC_DOSP_DROP0
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FWPM_NET_EVENT_IPSEC_DOSP_DROP0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_IPSEC_DOSP_DROP0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_IPSEC_DOSP_DROP0_ structure


## -description


The <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP0</b> structure contains information that describes an IPsec DoS Protection drop event.


## -struct-fields




### -field ipVersion

Internet Protocol (IP) version.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a> for more information.


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

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552433">FWP_DIRECTION</a> value that specifies whether the dropped packet is inbound or outbound.


## -remarks



<b>FWPM_NET_EVENT_IPSEC_DOSP_DROP0</b> is a specific implementation of FWPM_NET_EVENT_IPSEC_DOSP_DROP. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552433">FWP_DIRECTION</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

