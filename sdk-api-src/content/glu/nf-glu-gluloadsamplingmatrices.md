---
UID: NF:glu.gluLoadSamplingMatrices
title: gluLoadSamplingMatrices function
author: windows-driver-content
description: The gluLoadSamplingMatrices function loads Non-Uniform Rational B-Spline (NURBS) sampling and culling matrices.
old-location: opengl\gluloadsamplingmatrices.htm
old-project: OpenGL
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluLoadSamplingMatrices, glu/gluLoadSamplingMatrices, gluLoadSamplingMatrices, gluLoadSamplingMatrices function [OpenGL], opengl.gluloadsamplingmatrices"
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
-	gluLoadSamplingMatrices
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluLoadSamplingMatrices function


## -description


The <b>gluLoadSamplingMatrices</b> function loads Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) sampling and culling matrices.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param modelMatrix

A modelview matrix (as from a <a href="https://msdn.microsoft.com/1701ae76-c60d-431d-8d37-a0a388a44bbc">glGetFloatv</a> call).


### -param projMatrix

A projection matrix (as from a <b>glGetFloatv</b> call).


### -param viewport

A viewport (as from a <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetIntegerv</a> call).


## -returns



This function does not return a value.




## -remarks



The <b>gluLoadSamplingMatrices</b> function uses <i>modelMatrix</i>, <i>projMatrix</i>, and <i>viewport</i> to recompute the sampling and culling matrices stored in <i>nobj</i>. The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU_SAMPLING_TOLERANCE property). The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU_CULLING property is turned on).

The <b>gluLoadSamplingMatrices</b> function is necessary only if the GLU_AUTO_LOAD_MATRIX property is turned off (see <a href="https://msdn.microsoft.com/c8c3b0c3-11b8-4123-91b6-75fed78932ce">gluNurbsProperty</a>). Although it can be convenient to leave the GLU_AUTO_LOAD_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)




## -see-also




<a href="https://msdn.microsoft.com/1701ae76-c60d-431d-8d37-a0a388a44bbc">glGetFloatv</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetIntegerv</a>



<a href="https://msdn.microsoft.com/7dbc75a0-d04e-4794-b3dd-a602addf9dfa">gluGetNurbsProperty</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>
 

 

