---
UID: NS:ipsectypes.IPSEC_V4_UDP_ENCAPSULATION0_
title: IPSEC_V4_UDP_ENCAPSULATION0_
author: windows-sdk-content
description: Stores the User Datagram Protocol (UDP) encapsulation ports for Encapsulating Security Payload (ESP) encapsulation.
old-location: fwp\ipsec_v4_udp_encapsulation0_struct.htm
old-project: FWP
ms.assetid: 69cddec0-7311-4833-8b24-293ad714054e
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_V4_UDP_ENCAPSULATION0, IPSEC_V4_UDP_ENCAPSULATION0 structure [Filtering], IPSEC_V4_UDP_ENCAPSULATION0_, fwp.ipsec_v4_udp_encapsulation0_struct, ipsectypes/IPSEC_V4_UDP_ENCAPSULATION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: IPSEC_V4_UDP_ENCAPSULATION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_V4_UDP_ENCAPSULATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_V4_UDP_ENCAPSULATION0_ structure


## -description


The <b>IPSEC_V4_UDP_ENCAPSULATION0</b> structure stores the User Datagram Protocol (UDP) encapsulation ports for Encapsulating Security Payload (ESP) encapsulation.


## -struct-fields




### -field localUdpEncapPort

Source UDP encapsulation port.


### -field remoteUdpEncapPort

Destination UDP encapsulation port.


## -remarks



This is used only when a NAT was detected as part of the IPsec NAT traversal specification.

<b>IPSEC_V4_UDP_ENCAPSULATION0</b> is a specific implementation of IPSEC_V4_UDP_ENCAPSULATION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

