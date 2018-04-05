---
UID: NF:glu.gluTessVertex
title: gluTessVertex function
author: windows-driver-content
description: The gluTessVertex function specifies a vertex on a polygon.
old-location: opengl\glutessvertex.htm
old-project: OpenGL
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluTessVertex, glu/gluTessVertex, gluTessVertex, gluTessVertex function [OpenGL], opengl.glutessvertex"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: glu.h
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
-	glu32.dll
api_name:
-	gluTessVertex
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessVertex function


## -description


The <b>gluTessVertex</b> function specifies a vertex on a polygon.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param coords

The location of the vertex.


### -param data

An pointer passed back to the program with the vertex callback (as specified by <a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>).


## -returns



This function does not return a value.




## -remarks



The <b>gluTessVertex</b> function describes a vertex on a polygon that the user is defining. Successive <b>gluTessVertex</b> calls describe a closed contour. For example, to describe a quadrilateral, call <b>gluTessVertex</b> four times. You can only call <b>gluTessVertex</b> between <a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a> and <a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a>.

The <i>data</i> parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal. This pointer is passed back to the program through the GLU_VERTEX callback after tessellation (see <a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>).




## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>



<a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>



<a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a>



<a href="https://msdn.microsoft.com/8c3a90d3-760d-4a0a-9808-a797383fcc42">gluTessNormal</a>



<a href="https://msdn.microsoft.com/1306b9ef-4f1e-4684-99ea-464bae1d0a61">gluTessProperty</a>
 

 

