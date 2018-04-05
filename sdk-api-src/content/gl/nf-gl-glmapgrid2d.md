---
UID: NF:gl.glMapGrid2d
title: glMapGrid2d function
author: windows-driver-content
description: Defines a one-dimensional mesh.
old-location: opengl\glmapgrid2d.htm
old-project: OpenGL
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glMapGrid2d, glMapGrid2d, glMapGrid2d function [OpenGL], opengl.glmapgrid2d
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Opengl32.dll
api_name:
-	glMapGrid2d
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glMapGrid2d function


## -description


Defines a one-dimensional mesh.


## -parameters




### -param un

The number of partitions in the grid range interval [u1, u2]. This value must be positive.


### -param u1

A value used as the mapping for integer grid domain value i = 0. 


### -param u2

A value used as the mapping for integer grid domain value i = un.


### -param vn

The number of partitions in the grid range interval [v1, v2].


### -param v1

A value used as the mapping for integer grid domain value j = 0.


### -param v2

A value used as the mapping for integer grid domain value j = vn.


## -returns



This function does not return a value.




## -remarks



The <b>glMapGrid</b> and <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a> functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values. The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.



The <a href="https://msdn.microsoft.com/a0bc822e-dd98-4586-a322-2779e11f38ca">glMapGrid1</a> and <b>glMapGrid2</b> functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a> for details of how u and v coordinates are evaluated.



The <a href="https://msdn.microsoft.com/a0bc822e-dd98-4586-a322-2779e11f38ca">glMapGrid1</a> function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate <i>un</i> maps exactly to <i>u2</i>. All other integer grid coordinates <i>i</i> are mapped such that:



<i>u = i(u2 u1)/un + u1</i>



The <b>glMapGrid2</b> function specifies two such linear mappings. One maps integer grid coordinate <i>i = 0</i> exactly to <i>u1</i>, and integer grid coordinate <i>i = un</i> exactly to <i>u2</i>. The other maps integer grid coordinate <i>j = 0</i> exactly to <i>v1</i>, and integer grid coordinate <i>j = vn</i> exactly to <i>v2</i>. Other integer grid coordinates i and j are mapped such that



<i>u = i(u2 u1)/un + u1</i>

<i>v = j (v2 v1)/vn + v1</i>



The mappings specified by <a href="https://msdn.microsoft.com/a0bc822e-dd98-4586-a322-2779e11f38ca">glMapGrid</a> are used identically by <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a> and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>.



The following functions retrieve information related to <a href="https://msdn.microsoft.com/a0bc822e-dd98-4586-a322-2779e11f38ca">glMapGrid</a>:



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a>



<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>



<a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>



<a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>
 

 

