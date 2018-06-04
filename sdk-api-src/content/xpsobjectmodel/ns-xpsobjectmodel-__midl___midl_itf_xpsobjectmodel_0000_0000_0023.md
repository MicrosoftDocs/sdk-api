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

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0023 structure


## -description


Describes the left two columns of a 3-by-3 matrix.


## -struct-fields




### -field m11

The value in the left column of the first row of the matrix.


### -field m12

The value in the center column of the first row of the matrix.


### -field m21

The value in the left column of the second row of the matrix.


### -field m22

The value in the center column of the second row of the matrix.


### -field m31

The value in the left column of the third row of the matrix. This value is also the x-offset.


### -field m32

The value in the center column of the third row of the matrix. This value is also the y-offset.


## -remarks



The values in the third column of the matrix are assumed to be 0, 0, 1.

The following table shows the entire matrix.

<table>
<tr>
<td>m11</td>
<td>m12</td>
<td> 0 </td>
</tr>
<tr>
<td>m21</td>
<td>m22</td>
<td> 0 </td>
</tr>
<tr>
<td>m31</td>
<td>m32</td>
<td> 1 </td>
</tr>
</table>
 




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

