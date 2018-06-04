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

# LPtoDP function


## -description


The <b>LPtoDP</b> function converts logical coordinates into device coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppt

TBD


### -param c

TBD




#### - lpPoints [in, out]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures. The x-coordinates and y-coordinates contained in each of the <b>POINT</b> structures will be transformed.


#### - nCount [in]

The number of points in the array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>LPtoDP</b> function fails if the logical coordinates exceed 32 bits, or if the converted device coordinates exceed 27 bits. In the case of such an overflow, the results for all the points are undefined.

<b>LPtoDP</b> calculates complex floating-point arithmetic, and it has a caching system for efficiency. Therefore, the conversion result of an initial call to <b>LPtoDP</b> might not exactly match the conversion result of a later call to <b>LPtoDP</b>. We recommend not to write code that relies on the exact match of the conversion results from multiple calls to <b>LPtoDP</b> even if the parameters that are passed to each call are identical.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/0106867c-e8c5-4826-8cba-60c29e1d021a">DPtoLP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>
 

 

