---
UID: NS:lpmapi.RSVP_HOP
title: RSVP_HOP
author: windows-sdk-content
description: The RSVP_HOP structure contains information about an RSVP-enabled hop.
old-location: qos\rsvp_hop.htm
tech.root: QOS
ms.assetid: 4b23bc0e-ccea-4161-93fa-b136099e88bd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RSVP_HOP, RSVP_HOP structure [QOS], lpmapi/RSVP_HOP, qos.rsvp_hop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lpmapi.h
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
 - Lpmapi.h
api_name:
 - RSVP_HOP
product: Windows
targetos: Windows
req.typenames: RSVP_HOP
req.redist: 
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
 

 

