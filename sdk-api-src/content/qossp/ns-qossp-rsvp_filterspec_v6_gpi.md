---
UID: NS:qossp._RSVP_FILTERSPEC_V6_GPI
title: RSVP_FILTERSPEC_V6_GPI (qossp.h)
author: windows-sdk-content
description: The RSVP_FILTERSPEC_V6_GPI structure provides general port identifier information for a given FILTERSPEC on an IPv6 address.
old-location: qos\rsvp_filterspec_v6_gpi.htm
tech.root: QOS
ms.assetid: ede040f4-4858-42d8-a4b5-af6e79c036d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPRSVP_FILTERSPEC_V6_GPI, *LPRSVP_FILTERSPEC_V6_GPI structure [QOS], RSVP_FILTERSPEC_V6_GPI, RSVP_FILTERSPEC_V6_GPI structure [QOS], qos.rsvp_filterspec_v6_gpi, qossp/*LPRSVP_FILTERSPEC_V6_GPI, qossp/RSVP_FILTERSPEC_V6_GPI"
ms.topic: struct
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Qossp.h
api_name:
 - RSVP_FILTERSPEC_V6_GPI
product: Windows
targetos: Windows
req.typenames: RSVP_FILTERSPEC_V6_GPI, *LPRSVP_FILTERSPEC_V6_GPI
req.redist: 
---

# RSVP_FILTERSPEC_V6_GPI structure


## -description


The <b>RSVP_FILTERSPEC_V6_GPI</b> structure provides general port identifier information for a given FILTERSPEC on an IPv6 address.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC general port identifier applies, expressed as an <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a> structure.


### -field GeneralPortId

General Port Identifier for the FILTERSPEC.


## -remarks



When working with IPv4 addresses, use <a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>.




## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>



<a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>
 

 

