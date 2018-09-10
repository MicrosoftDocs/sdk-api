---
UID: NS:qossp._RSVP_FILTERSPEC
title: "_RSVP_FILTERSPEC"
author: windows-sdk-content
description: The RSVP_FILTERSPEC structure provides RSVP FILTERSPEC information.
old-location: qos\rsvp_filterspec.htm
tech.root: QOS
ms.assetid: ce4af25d-6c31-43a2-a30a-1d28b18e8f8b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPRSVP_FILTERSPEC, *LPRSVP_FILTERSPEC structure [QOS], RSVP_FILTERSPEC, RSVP_FILTERSPEC structure [QOS], _RSVP_FILTERSPEC, qos.rsvp_filterspec, qossp/*LPRSVP_FILTERSPEC, qossp/RSVP_FILTERSPEC"
ms.prod: windows
ms.technology: windows-sdk
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
 - RSVP_FILTERSPEC
product: Windows
targetos: Windows
req.typenames: RSVP_FILTERSPEC, *LPRSVP_FILTERSPEC
req.redist: 
---

# _RSVP_FILTERSPEC structure


## -description


The <b>RSVP_FILTERSPEC</b> structure provides RSVP FILTERSPEC information.


## -struct-fields




### -field Type

Specifies the type of FILTERSPEC using the <b>FilterSpec</b> enumeration.


### -field FilterSpecV4

IPv4 FILTERSPEC information, provided in the form of a <a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a> structure.


### -field FilterSpecV6

IPv6 FILTERSPEC information, provided in the form of a <a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a> structure.


### -field FilterSpecV6Flow

IPv6 FILTERSPEC flow information, provided in the form of a <a href="https://msdn.microsoft.com/5bca12be-5bc4-40b2-bc72-52cf0297821b">RSVP_FILTERSPEC_V6_FLOW</a> structure.


### -field FilterSpecV4Gpi

IPv4 FILTERSPEC general port ID information, provided in the form of a <a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a> structure.


### -field FilterSpecV6Gpi

IPv6 FILTERSPEC general port ID information, provided in the form of a <a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>



<a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>



<a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a>



<a href="https://msdn.microsoft.com/5bca12be-5bc4-40b2-bc72-52cf0297821b">RSVP_FILTERSPEC_V6_FLOW</a>



<a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a>
 

 

