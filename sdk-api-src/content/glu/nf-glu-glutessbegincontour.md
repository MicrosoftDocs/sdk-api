---
UID: NF:glu.gluTessBeginContour
title: gluTessBeginContour function
author: windows-driver-content
description: The gluTessBeginContour and gluTessEndContour functions delimit a contour description.
old-location: opengl\glutessbegincontour.htm
old-project: OpenGL
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: glu/gluTessBeginContour, gluTessBeginContour, gluTessBeginContour function [OpenGL], opengl.glutessbegincontour
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
-	Glu32.dll
api_name:
-	gluTessBeginContour
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessBeginContour function


## -description


The <b>gluTessBeginContour</b> and <a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a> functions delimit a contour description.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


## -returns



This function does not return a value.




## -remarks



The <b>gluTessBeginContour</b> and <a href="https://msdn.microsoft.com/c9ae2075-59d7-4c1a-b720-0aa05954525c">gluTessEndPolygon</a> functions delimit the definition of a polygon contour. Within each <b>gluTessBeginContour</b>/<b>gluTessEndPolygon</b> pair, there can be zero or more calls to <a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>. The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first). You can call <b>gluTessBeginContour</b> only between <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a> and <b>gluTessEndPolygon</b>.




## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>



<a href="https://msdn.microsoft.com/c9ae2075-59d7-4c1a-b720-0aa05954525c">gluTessEndPolygon</a>



<a href="https://msdn.microsoft.com/8c3a90d3-760d-4a0a-9808-a797383fcc42">gluTessNormal</a>



<a href="https://msdn.microsoft.com/1306b9ef-4f1e-4684-99ea-464bae1d0a61">gluTessProperty</a>



<a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>
 

 

