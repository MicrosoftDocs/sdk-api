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

# IDirectDraw7::GetScanLine


## -description


Retrieves the scan line that is currently being drawn on the monitor.


## -parameters






#### - lpdwScanLine [out]

A pointer to a variable that receives the scan line that the display is currently drawing.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_VERTICALBLANKINPROGRESS</li>
</ul>



## -remarks



Scan lines are reported as zero-based integers. The returned scan line value is in the range from 0 through n, where 0 is the first visible scan line on the screen and n is the last visible scan line, plus any scan lines that occur during the vertical blank period. So, in a case where an application is running at a resolution of 640×480 and there are 12 scan lines during vblank, the values returned by this method range from 0 through 491.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <a href="https://msdn.microsoft.com/13f8e5c2-b957-43ce-9fc8-5554c2321bdd">GetMonitorFrequency</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

