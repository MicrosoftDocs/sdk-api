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

# IDirectDrawGammaControl::GetGammaRamp


## -description


Retrieves the red, green, and blue gamma ramps for the primary surface.


## -parameters




### -param






#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lpRampData [in, out]

A pointer to a <a href="https://msdn.microsoft.com/ec4cb111-3b12-4470-b1e3-e4379f7f2632">DDGAMMARAMP</a> structure that receives the current red, green, and blue gamma ramps. Each array maps color values in the frame buffer to the color values to be passed to the digital-to-analog converter (DAC).


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetGammaRamp</b> method.




## -see-also




<a href="https://msdn.microsoft.com/a6286a2d-76d5-49ec-afd5-cbf112528db8">IDirectDrawGammaControl</a>
 

 

