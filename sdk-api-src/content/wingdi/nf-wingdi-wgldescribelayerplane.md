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

# wglDescribeLayerPlane function


## -description


The <b>wglDescribeLayerPlane</b> function obtains information about the layer planes of a given pixel format.


## -parameters




### -param

TBD




#### - hdc

Specifies the device context of a window whose layer planes are to be described.


#### - iLayerPlane

Specifies the overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure.


#### - iPixelFormat

Specifies which layer planes of a pixel format are being described.


#### - nBytes

Specifies the size, in bytes, of the structure pointed to by <i>plpd</i>. The <b>wglDescribeLayerPlane</b> function stores layer plane data in a <a href="https://msdn.microsoft.com/fdb0322d-503f-4c17-b438-f764d60da7f6">LAYERPLANEDESCRIPTOR</a> structure, and stores no more than <i>nBytes</i> of data. Set the value of <i>nBytes</i> to the size of <b>LAYERPLANEDESCRIPTOR</b>.


#### - plpd

Points to a <b>LAYERPLANEDESCRIPTOR</b> structure. The <b>wglDescribeLayerPlane</b> function sets the value of the structure's data members. The function stores the number of bytes of data copied to the structure in the <b>nSize</b> member.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. In addition, the <b>wglDescribeLayerPlane</b> function sets the members of the <b>LAYERPLANEDESCRIPTOR</b> structure pointed to by <i>plpd</i> according to the specified layer plane (<i>iLayerPlane</i> ) of the specified pixel format (<i>iPixelFormat</i> ).

If the function fails, the return value is <b>FALSE</b>.




## -remarks



The numbering of planes (<i>iLayerPlane</i> ) determines their order. Higher-numbered planes overlay lower-numbered planes.




## -see-also




<a href="https://msdn.microsoft.com/9692a30d-c7d4-40c7-a265-72c4ebabd5f2">DescribePixelFormat</a>



<a href="https://msdn.microsoft.com/fdb0322d-503f-4c17-b438-f764d60da7f6">LAYERPLANEDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/81050b48-7385-4ef3-acc5-82d5c893b2e8">wglCreateLayerContext</a>
 

 

