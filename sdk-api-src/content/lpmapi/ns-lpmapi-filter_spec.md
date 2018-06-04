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

# FILTER_SPEC structure


## -description


The 
<b>FILTER_SPEC</b> structure stores information about an RSVP FILTERSPEC.


## -struct-fields




### -field filt_header

RSVP Object Header for the FILTERSPEC, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field filt_u


### -field filt_u.filt_ipv4

FILTERSPEC, in the form of a <a href="https://msdn.microsoft.com/b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e">Filter_Spec_IPv4</a> header.


### -field filt_u.filt_ipv4gpi

FILTERSPEC GPI information, in the form of a <a href="https://msdn.microsoft.com/c1546673-d1b5-4a7f-82d0-a8cc1c7c8752">Filter_Spec_IPv4GPI</a> header.


## -see-also




<a href="https://msdn.microsoft.com/b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e">Filter_Spec_IPv4</a>



<a href="https://msdn.microsoft.com/c1546673-d1b5-4a7f-82d0-a8cc1c7c8752">Filter_Spec_IPv4GPI</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

