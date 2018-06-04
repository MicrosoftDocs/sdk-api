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

# IDirectManipulationPrimaryContent::SetSnapCoordinate


## -description


    Specifies the coordinate system for snap points or snap intervals. 


## -parameters




### -param motion [in]

One of the values from <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a>. 


### -param coordinate [in]

One of the values from <a href="https://msdn.microsoft.com/954ab792-e2b9-4cc0-a0dc-fcb6c6cdf156">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a>. 

If <i>motion</i> is set to translation (<b>DIRECTMANIPULATION_MOTION_TRANSLATEX</b> or <b>DIRECTMANIPULATION_MOTION_TRANSLATEY</b>), all values of <a href="https://msdn.microsoft.com/954ab792-e2b9-4cc0-a0dc-fcb6c6cdf156">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a> are valid. 

If <i>motion</i> is set to <b>DIRECTMANIPULATION_MOTION_ZOOM</b>, only <b>DIRECTMANIPULATION_COORDINATE_ORIGIN</b> of <a href="https://msdn.microsoft.com/954ab792-e2b9-4cc0-a0dc-fcb6c6cdf156">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a> is valid (<i>origin</i> must be set to 0.0f).


### -param origin [in]

The initial, or starting, snap point. All snap points are relative to this one. Only used when  <a href="https://msdn.microsoft.com/954ab792-e2b9-4cc0-a0dc-fcb6c6cdf156">DIRECTMANIPULATION_COORDINATE_ORIGIN</a> is set. 

If <i>motion</i> is set to <b>DIRECTMANIPULATION_MOTION_ZOOM</b>, then <i>origin</i> must be set to 0.0f.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The origin is relative to the content boundaries. If no boundary has been set (<a href="https://msdn.microsoft.com/41b14e56-ba24-4ad2-9dac-28daf7d13c6a">SetContentRect</a> is never called) the default boundaries are (-<a href="_pluslang_Floating_Limits">FLT_MAX</a>, <a href="_pluslang_Floating_Limits">FLT_MAX</a>). 




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>



<a href="https://msdn.microsoft.com/99d039fe-017a-47c5-95a1-5000efe92ba0">SetSnapInterval</a>



<a href="https://msdn.microsoft.com/3257952d-903b-455c-9422-9739411a5924">SetSnapPoints</a>
 

 

