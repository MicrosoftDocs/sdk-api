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

# tagXFORM structure


## -description



The <b>XFORM</b> structure specifies a world-space to page-space transformation.




## -struct-fields




### -field eM11

The following.

<table>
<tr>
<th>Operation</th>
<th>Meaning</th>
</tr>
<tr>
<td>Scaling</td>
<td>Horizontal scaling component</td>
</tr>
<tr>
<td>Rotation</td>
<td>Cosine of rotation angle</td>
</tr>
<tr>
<td>Reflection</td>
<td>Horizontal component</td>
</tr>
</table>
 


### -field eM12

The following.

<table>
<tr>
<th>Operation</th>
<th>Meaning</th>
</tr>
<tr>
<td>Shear</td>
<td>Horizontal proportionality constant</td>
</tr>
<tr>
<td>Rotation</td>
<td>Sine of the rotation angle</td>
</tr>
</table>
 


### -field eM21

The following.

<table>
<tr>
<th>Operation</th>
<th>Meaning</th>
</tr>
<tr>
<td>Shear</td>
<td>Vertical proportionality constant</td>
</tr>
<tr>
<td>Rotation</td>
<td>Negative sine of the rotation angle</td>
</tr>
</table>
 


### -field eM22

The following.

<table>
<tr>
<th>Operation</th>
<th>Meaning</th>
</tr>
<tr>
<td>Scaling</td>
<td>Vertical scaling component</td>
</tr>
<tr>
<td>Rotation</td>
<td>Cosine of rotation angle</td>
</tr>
<tr>
<td>Reflection</td>
<td>Vertical reflection component</td>
</tr>
</table>
 


### -field eDx

The horizontal translation component, in logical units.


### -field eDy

The vertical translation component, in logical units.


## -remarks



The following list describes how the members are used for each operation.

<table>
<tr>
<th>Operation</th>
<th>eM11</th>
<th>eM12</th>
<th>eM21</th>
<th>eM22</th>
</tr>
<tr>
<td>Rotation</td>
<td>Cosine</td>
<td>Sine</td>
<td>Negative sine</td>
<td>Cosine</td>
</tr>
<tr>
<td>Scaling</td>
<td>Horizontal scaling component</td>
<td>Not used</td>
<td>Not used</td>
<td>Vertical Scaling Component</td>
</tr>
<tr>
<td>Shear</td>
<td>Not used</td>
<td>Horizontal Proportionality Constant</td>
<td>Vertical Proportionality Constant</td>
<td>Not used</td>
</tr>
<tr>
<td>Reflection</td>
<td>Horizontal Reflection Component</td>
<td>Not used</td>
<td>Not used</td>
<td>Vertical Reflection Component</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8715ca4f-5e39-494f-80a5-db3a2f7e620a">Coordinate Space and Transformation Structures</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/4dcff824-eb1d-425c-b246-db4ace2c6518">ExtCreateRegion</a>



<a href="https://msdn.microsoft.com/72945b1e-144e-4724-bf08-6f971f8adb43">GetWorldTransform</a>



<a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>



<a href="https://msdn.microsoft.com/d103a4dd-949e-4f18-ac90-bb0e51011233">SetWorldTransform</a>
 

 

