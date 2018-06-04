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

# D2D1GetGradientMeshInteriorPointsFromCoonsPatch function


## -description


Returns the interior points for a gradient mesh patch based on the points defining a Coons patch.<div class="alert"><b>Note</b>  <p class="note">This function is called by the <a href="https://msdn.microsoft.com/12469ab9-890c-e4a9-57b2-41a804712052">GradientMeshPatchFromCoonsPatch</a> function and is not intended to be used directly.

</div>
<div> </div>



## -parameters




### -param pPoint0

TBD


### -param pPoint1

TBD


### -param pPoint2

TBD


### -param pPoint3

TBD


### -param pPoint4

TBD


### -param pPoint5

TBD


### -param pPoint6

TBD


### -param pPoint7

TBD


### -param pPoint8

TBD


### -param pPoint9

TBD


### -param pPoint10

TBD


### -param pPoint11

TBD


### -param pTensorPoint11 [out]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point11 in the <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint12 [out]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point12 in the <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint21 [out]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point21 in the <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint22 [out]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point22 in the <a href="https://msdn.microsoft.com/16d1ef03-f0c9-7414-d54d-9513199272aa">D2D1_GRADIENT_MESH_PATCH</a> structure.


#### - point0 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 0.


#### - point1 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 1.


#### - point10 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 10.


#### - point11 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 11.


#### - point2 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 2.


#### - point3 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 3.


#### - point4 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 4.


#### - point5 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 5.


#### - point6 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 6.


#### - point7 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 7.


#### - point8 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 8.


#### - point9 [in]

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 9.


## -returns



This function does not return a value.




## -remarks



This function is called by the <a href="https://msdn.microsoft.com/12469ab9-890c-e4a9-57b2-41a804712052">GradientMeshPatchFromCoonsPatch</a> function and is not intended to be used directly.



