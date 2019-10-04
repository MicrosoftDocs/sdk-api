---
UID: NS:ipsectypes.IPSEC_V4_UDP_ENCAPSULATION0_
title: IPSEC_V4_UDP_ENCAPSULATION0 (ipsectypes.h)
author: windows-sdk-content
description: Stores the User Datagram Protocol (UDP) encapsulation ports for Encapsulating Security Payload (ESP) encapsulation.
old-location: fwp\ipsec_v4_udp_encapsulation0_struct.htm
tech.root: fwp
ms.assetid: 69cddec0-7311-4833-8b24-293ad714054e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_V4_UDP_ENCAPSULATION0, IPSEC_V4_UDP_ENCAPSULATION0 structure [Filtering], IPSEC_V4_UDP_ENCAPSULATION0_, fwp.ipsec_v4_udp_encapsulation0_struct, ipsectypes/IPSEC_V4_UDP_ENCAPSULATION0
ms.topic: struct
f1_keywords: 
 - "ipsectypes/IPSEC_V4_UDP_ENCAPSULATION0"
dev_langs:
 - c++
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_V4_UDP_ENCAPSULATION0
targetos: Windows
req.typenames: IPSEC_V4_UDP_ENCAPSULATION0
req.redist: 
ms.custom: 19H1
---

# IPSEC_V4_UDP_ENCAPSULATION0 structure


## -description


The <b>IPSEC_V4_UDP_ENCAPSULATION0</b> structure stores the User Datagram Protocol (UDP) encapsulation ports for Encapsulating Security Payload (ESP) encapsulation.


## -struct-fields




### -field localUdpEncapPort

Source UDP encapsulation port.


### -field remoteUdpEncapPort

Destination UDP encapsulation port.


## -remarks



This is used only when a NAT was detected as part of the IPsec NAT traversal specification.

<b>IPSEC_V4_UDP_ENCAPSULATION0</b> is a specific implementation of IPSEC_V4_UDP_ENCAPSULATION. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

