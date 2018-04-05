---
UID: NF:gl.glEdgeFlagv
title: glEdgeFlagv function
author: windows-driver-content
description: Flags edges as either boundary or nonboundary.
old-location: opengl\gledgeflagv.htm
old-project: OpenGL
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEdgeFlagv, glEdgeFlagv, glEdgeFlagv function [OpenGL], opengl.gledgeflagv
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
-	opengl32.dll
api_name:
-	glEdgeFlagv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEdgeFlagv function


## -description


Flags edges as either boundary or nonboundary.


## -parameters




### -param flag

Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value. 


## -returns



This function does not return a value.




## -remarks



Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>/<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> pair is marked as the start of either a boundary or nonboundary edge. If the current edge flag is <b>TRUE</b> when the vertex is specified, the vertex is marked as the start of a boundary edge. If the current edge flag is <b>FALSE</b>, the vertex is marked as the start of a nonboundary edge. The <b>glEdgeFlagv</b> function sets the edge flag to <b>TRUE</b> if flag is nonzero, <b>FALSE</b> otherwise.

The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.

Boundary and nonboundary edge flags on vertices are significant only if GL_POLYGON_MODE is set to GL_POINT or GL_LINE. See <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>. 

Initially, the edge flag bit is <b>TRUE</b>.

The current edge flag can be updated at any time. In particular, <b>glEdgeFlagv</b> can be called between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>.

The following functions retrieve information related to <b>glEdgeFlagv</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_EDGE_FLAG



