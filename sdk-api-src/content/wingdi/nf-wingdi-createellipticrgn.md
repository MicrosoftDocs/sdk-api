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

# CreateEllipticRgn function


## -description


The <b>CreateEllipticRgn</b> function creates an elliptical region.


## -parameters




### -param x1

TBD


### -param y1

TBD


### -param x2

TBD


### -param y2

TBD




#### - nBottomRect [in]

Specifies the y-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.


#### - nLeftRect [in]

Specifies the x-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.


#### - nRightRect [in]

Specifies the x-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.


#### - nTopRect [in]

Specifies the y-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the HRGN object, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

A bounding rectangle defines the size, shape, and orientation of the region: The long sides of the rectangle define the length of the ellipse's major axis; the short sides define the length of the ellipse's minor axis; and the center of the rectangle defines the intersection of the major and minor axes.




## -see-also




<a href="https://msdn.microsoft.com/bd30516e-1e05-4b7d-a6bf-7512cf3ef30f">CreateEllipticRegnIndirect</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

