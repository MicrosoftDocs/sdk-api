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

# IAMPhysicalPinInfo::GetPhysicalType


## -description



<div class="alert"><b>Note</b>  The <code>IAMPhysicalPinInfo</code> interface is deprecated.</div>
<div> </div>
Retrieves the type and name of the physical pin.




## -parameters




### -param pType [out]

Pointer to a variable that receives a value indicating the pin's type. The <a href="https://msdn.microsoft.com/00635c01-f068-43b0-b7b6-d26f27886f71">PhysicalConnectorType</a> enumeration defines the pin type values.


### -param ppszType [out]

Address of a pointer to a buffer that receives a human-readable string identifying the pin type.


## -returns



Returns S_OK if a valid physical pin value is found. Otherwise, returns VFW_E_NO_ACCEPTABLE_TYPES.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d1d05d2c-018e-421f-bfb9-810d708f726c">IAMPhysicalPinInfo Interface</a>
 

 

