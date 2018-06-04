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

# RSVP_HOP structure


## -description


The 
<b>RSVP_HOP</b> structure contains information about an RSVP-enabled hop.


## -struct-fields




### -field hop_header

RSVP hop header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure


### -field hop_u


### -field hop_u.hop_ipv4

Information about the IPv4 hop, in the form of an <a href="https://msdn.microsoft.com/1a3f3e65-70f8-490c-8724-9e93c7fba457">Rsvp_Hop_IPv4</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>



<a href="https://msdn.microsoft.com/1a3f3e65-70f8-490c-8724-9e93c7fba457">Rsvp_Hop_IPv4</a>
 

 

