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

# FONTOBJ_pxoGetXform function


## -description


The <b>FONTOBJ_pxoGetXform</b> function retrieves the notional-to-device transform for the specified font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure for which the transform is to be retrieved.


## -returns



The return value is a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure that describes the transform. The XFORMOBJ structure can be used by the <b>XFORMOBJ_</b><b><i>Xxx</i></b> service routines. The XFORMOBJ structure assumes that: 

<ul>
<li>The distance between the pixels is in device space units. </li>
<li>Both notional and device space have positive values of y in the top-to-bottom direction. </li>
</ul>
If the font is a raster font, the return value is <b>NULL</b>.




## -remarks



The driver needs the notional-to-device transform to realize a driver-supplied font.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>
 

 

