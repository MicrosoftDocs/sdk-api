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

# SENDER_TSPEC structure


## -description


The 
<b>SENDER_TSPEC</b> structure contains information for an RSVP sender Tspec.


## -struct-fields




### -field stspec_header

Object header, expressed as an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field stspec_body

Sender Tspec body information, expressed as an <a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c4244dba-237a-437b-94b7-fd814edb3506">IntServTspecBody</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

