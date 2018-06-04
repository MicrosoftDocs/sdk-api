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

# FWPM_FIELD0_ structure


## -description


The <b>FWPM_FIELD0</b> structure specifies schema information for a field. 


## -struct-fields




### -field fieldKey

Uniquely identifies the field. See FWPM_CONDITION_* identifiers in the topic <a href="https://msdn.microsoft.com/library/windows/hardware/ff549944">Filtering Condition Identifiers</a>.


### -field type

Determines how <b>dataType</b> is interpreted.

See <a href="https://msdn.microsoft.com/46983847-7c68-4ee7-946e-ea62f34d1a38">FWPM_FIELD_TYPE</a> for more information.


### -field dataType

Data type passed to classify.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552431">FWP_DATA_TYPE</a> for more information.


## -remarks



<b>FWPM_FIELD0</b> is a specific implementation of FWPM_FIELD. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/46983847-7c68-4ee7-946e-ea62f34d1a38">FWPM_FIELD_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552431">FWP_DATA_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

