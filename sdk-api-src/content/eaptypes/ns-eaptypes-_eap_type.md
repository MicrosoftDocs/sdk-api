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

# _EAP_TYPE structure


## -description


The <b>EAP_TYPE</b> structure contains type and vendor identification information for an EAP method.


## -struct-fields




### -field type

The numeric type code for this EAP method.

<div class="alert"><b>Note</b>  For more information on the allocation of EAP method types, see section 6.2 of <a href="Http://go.microsoft.com/fwlink/p/?linkid=84016">RFC 3748</a>.</div>
<div> </div>

### -field dwVendorId

The vendor ID for the EAP method.


### -field dwVendorType

The numeric type code for the vendor of this EAP method.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>
 

 

