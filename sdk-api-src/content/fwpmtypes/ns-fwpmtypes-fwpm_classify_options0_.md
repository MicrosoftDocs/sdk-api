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

# FWPM_CLASSIFY_OPTIONS0_ structure


## -description


 The <b>FWPM_CLASSIFY_OPTIONS0</b> structure is used to store <b>FWPM_CLASSIFY_OPTION0</b> structures.


## -struct-fields




### -field numOptions

Number of <b>FWPM_CLASSIFY_OPTION0</b> structures in the <b>options</b> member.


### -field options

[size_is(numCredentials)]

Pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a> structures.


## -remarks



<b>FWPM_CLASSIFY_OPTIONS0</b> is a specific implementation of FWPM_CLASSIFY_OPTIONS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

