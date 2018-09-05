---
UID: NS:qossp._RSVP_FILTERSPEC_V6_FLOW
title: "_RSVP_FILTERSPEC_V6_FLOW"
author: windows-sdk-content
description: The RSVP_FILTERSPEC_V6_FLOW structure provides flow label information for an IPv6 FILTERSPEC.
old-location: qos\rsvp_filterspec_v6_flow.htm
old-project: QOS
ms.assetid: 5bca12be-5bc4-40b2-bc72-52cf0297821b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPRSVP_FILTERSPEC_V6_FLOW, *LPRSVP_FILTERSPEC_V6_FLOW structure [QOS], RSVP_FILTERSPEC_V6_FLOW, RSVP_FILTERSPEC_V6_FLOW structure [QOS], _RSVP_FILTERSPEC_V6_FLOW, qos.rsvp_filterspec_v6_flow, qossp/*LPRSVP_FILTERSPEC_V6_FLOW, qossp/RSVP_FILTERSPEC_V6_FLOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: qossp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RSVP_FILTERSPEC_V6_FLOW, *LPRSVP_FILTERSPEC_V6_FLOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - RSVP_FILTERSPEC_V6_FLOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _RSVP_FILTERSPEC_V6_FLOW structure


## -description


The <b>RSVP_FILTERSPEC_V6_FLOW</b> structure provides flow label information for an IPv6 FILTERSPEC.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC flow label applies, expressed as an <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a> structure.


### -field UnUsed

 


### -field FlowLabel

Label for the flow.


#### - Unused

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>



<a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a>
 

 

