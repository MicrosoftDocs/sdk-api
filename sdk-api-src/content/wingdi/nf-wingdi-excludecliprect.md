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

# ExcludeClipRect function


## -description


The <b>ExcludeClipRect</b> function creates a new clipping region that consists of the existing clipping region minus the specified rectangle.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left

TBD


### -param top

TBD


### -param right

TBD


### -param bottom

TBD




#### - nBottomRect [in]

The y-coordinate, in logical units, of the lower-right corner of the rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical units, of the upper-left corner of the rectangle.


#### - nRightRect [in]

The x-coordinate, in logical units, of the lower-right corner of the rectangle.


#### - nTopRect [in]

The y-coordinate, in logical units, of the upper-left corner of the rectangle.


## -returns



The return value specifies the new clipping region's complexity; it can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULLREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is more than one rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
No region was created.

</td>
</tr>
</table>
 




## -remarks



The lower and right edges of the specified rectangle are not excluded from the clipping region.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/9b3f9bfb-337b-45f0-b9ec-399e5f563638">IntersectClipRect</a>
 

 

