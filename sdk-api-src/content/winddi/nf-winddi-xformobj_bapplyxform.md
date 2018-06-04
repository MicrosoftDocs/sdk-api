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

# XFORMOBJ_bApplyXform function


## -description


The <b>XFORMOBJ_bApplyXform</b> function applies the given transform or its inverse to the given array of points.


## -parameters




### -param pxo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure that defines the transform to be applied to the <i>pvIn</i> array.


### -param __out_validated

TBD


### -param cPoints

Specifies the count of points in <i>pvIn</i> to be transformed.


### -param pvIn

Pointer to an array of input points. The format of the points is specified by the <i>iMode</i> parameter.


### -param pvOut

Pointer to the buffer that is to receive the transformed points. The <i>iMode</i> parameter specifies the format of the points.


#### - iMode [in]

Identifies the transform and the input and output data types. This parameter can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
XF_INV_FXTOL

</td>
<td>
Applies the inverse of the transform to POINTFIX structures to get <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structures.

</td>
</tr>
<tr>
<td>
XF_INV_LTOL

</td>
<td>
Applies the inverse of the transform to POINTL structures to get POINTL structures.

</td>
</tr>
<tr>
<td>
XF_LTOFX

</td>
<td>
Applies the transform to POINTL structures to get POINTFIX structures (see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>).

</td>
</tr>
<tr>
<td>
XF_LTOL

</td>
<td>
Applies the transform to POINTL structures to get POINTL structures.

</td>
</tr>
</table>
 


## -returns



The return value is <b>TRUE</b> if all points were transformed without overflow. <b>FALSE</b> is returned if <i>pxo</i>, <i>pvIn</i>, or <i>pvOut</i> are <b>null</b>, or if overflow occurs during the transformation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>
 

 

