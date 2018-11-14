---
UID: NF:d2d1_3.D2D1GetGradientMeshInteriorPointsFromCoonsPatch
title: D2D1GetGradientMeshInteriorPointsFromCoonsPatch function
author: windows-sdk-content
description: Returns the interior points for a gradient mesh patch based on the points defining a Coons patch.
old-location: direct2d\d2d1getgradientmeshinteriorpointsfromcoonspatch.htm
tech.root: direct2d
ms.assetid: 388d5cbf-cb15-f0c9-3f3b-897f68519a4c
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D2D1GetGradientMeshInteriorPointsFromCoonsPatch, D2D1GetGradientMeshInteriorPointsFromCoonsPatch function [Direct2D], d2d1_3/D2D1GetGradientMeshInteriorPointsFromCoonsPatch, direct2d.d2d1getgradientmeshinteriorpointsfromcoonspatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - D2D1GetGradientMeshInteriorPointsFromCoonsPatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- D2D1GetGradientMeshInteriorPointsFromCoonsPatch
: 
---

# D2D1GetGradientMeshInteriorPointsFromCoonsPatch function


## -description


Returns the interior points for a gradient mesh patch based on the points defining a Coons patch.<div class="alert"><b>Note</b>  <p class="note">This function is called by the <a href="https://msdn.microsoft.com/en-us/library/Dn890772(v=VS.85).aspx">GradientMeshPatchFromCoonsPatch</a> function and is not intended to be used directly.

</div>
<div> </div>



## -parameters




### -param pPoint0 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 0.


### -param pPoint1 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 1.


### -param pPoint2 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 2.


### -param pPoint3 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 3.


### -param pPoint4 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 4.


### -param pPoint5 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 5.


### -param pPoint6 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 6.


### -param pPoint7 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 7.


### -param pPoint8 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 8.


### -param pPoint9 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 9.


### -param pPoint10 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 10.


### -param pPoint11 [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

The coordinate-space location of the control point at position 11.


### -param pTensorPoint11 [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point11 in the <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint12 [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point12 in the <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint21 [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point21 in the <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure.


### -param pTensorPoint22 [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a>*</b>

Returns the interior point for the gradient mesh corresponding to point22 in the <a href="https://msdn.microsoft.com/en-us/library/Dn890726(v=VS.85).aspx">D2D1_GRADIENT_MESH_PATCH</a> structure.


## -returns



This function does not return a value.




## -remarks



This function is called by the <a href="https://msdn.microsoft.com/en-us/library/Dn890772(v=VS.85).aspx">GradientMeshPatchFromCoonsPatch</a> function and is not intended to be used directly.



