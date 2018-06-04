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

# ERROR_SPEC structure


## -description


The 
<b>ERROR_SPEC</b> structure contains RSVP error messages.


## -struct-fields




### -field errs_header

Error header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field errs_u

Union containing RSVP error information.


### -field errs_u.errs_ipv4

Error information, expressed as an <a href="https://msdn.microsoft.com/23df7278-8f37-426f-98ff-0cf02d780b76">Error_Spec_IPv4</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/23df7278-8f37-426f-98ff-0cf02d780b76">Error_Spec_IPv4</a>



<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

