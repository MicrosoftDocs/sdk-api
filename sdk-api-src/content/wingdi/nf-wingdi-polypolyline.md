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

# PolyPolyline function


## -description


The <b>PolyPolyline</b> function draws multiple series of connected line segments.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param apt

TBD


### -param asz

TBD


### -param csz

TBD




#### - cCount [in]

The total number of entries in the <i>lpdwPolyPoints</i> array.


#### - lpdwPolyPoints [in]

A pointer to an array of variables specifying the number of points in the <i>lppt</i> array for the corresponding polyline. Each entry must be greater than or equal to two.


#### - lppt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures that contains the vertices of the polylines, in logical units. The polylines are specified consecutively.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The line segments are drawn by using the current pen. The figures formed by the segments are not filled.

The current position is neither used nor updated by this function.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
 

 

