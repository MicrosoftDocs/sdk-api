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

# FWP_RANGE0_ structure


## -description



		The <b>FWP_RANGE0</b> structure specifies a range of values.


## -struct-fields




### -field valueLow

Low value of the range.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> for more information.


### -field valueHigh

High value of the range.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> for more information.


## -remarks



The elements <b>valueLow</b> and <b>valueHigh</b> must be the same data type and 
<b>valueHigh</b> must be greater than or equal to <b>valueLow</b>. 

Ranges are always inclusive. Thus, if a value equals
<b>valueLow</b> or <b>valueHigh</b>, it is contained in the range.

<b>FWP_RANGE0</b> is a specific implementation of FWP_RANGE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

