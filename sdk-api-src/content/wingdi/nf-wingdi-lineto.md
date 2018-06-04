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

# LineTo function


## -description


The <b>LineTo</b> function draws a line from the current position up to, but not including, the specified point.


## -parameters




### -param hdc [in]

Handle to a device context.


### -param x

TBD


### -param y

TBD




#### - nXEnd [in]

Specifies the x-coordinate, in logical units, of the line's ending point.


#### - nYEnd [in]

Specifies the y-coordinate, in logical units, of the line's ending point.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The line is drawn by using the current pen and, if the pen is a geometric pen, the current brush.

If <b>LineTo</b> succeeds, the current position is set to the specified ending point.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/69114875-f3e0-45e9-8e87-1f4e9de08db1">Drawing Markers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
 

 

