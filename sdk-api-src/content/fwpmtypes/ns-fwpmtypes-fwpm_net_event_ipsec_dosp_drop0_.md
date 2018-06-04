---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

