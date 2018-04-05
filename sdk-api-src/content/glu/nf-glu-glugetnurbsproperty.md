---
UID: NF:glu.gluGetNurbsProperty
title: gluGetNurbsProperty function
author: windows-driver-content
description: The gluGetNurbsProperty function gets a Non-Uniform Rational B-Spline (NURBS) property.
old-location: opengl\glugetnurbsproperty.htm
old-project: OpenGL
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluGetNurbsProperty, glu/gluGetNurbsProperty, gluGetNurbsProperty, gluGetNurbsProperty function [OpenGL], opengl.glugetnurbsproperty"
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
-	gluGetNurbsProperty
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluGetNurbsProperty function


## -description


The <b>gluGetNurbsProperty</b> function gets a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) property.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param property

The property whose value is to be retrieved. The following values are valid: GLU_SAMPLING_TOLERANCE, GLU_DISPLAY_MODE, GLU_CULLING, GLU_AUTO_LOAD_MATRIX, GLU_PARAMETRIC_TOLERANCE, GLU_SAMPLING_METHOD, GLU_U_STEP, and GLU_V_STEP.


### -param value

A pointer to the location into which the value of the named property is written.


## -returns



This function does not return a value.




## -remarks



Use <b>gluGetNurbsProperty</b> to retrieve properties stored in a NURBS object. These properties affect the way NURBS curves and surfaces are rendered. For information about NURBS properties, see <a href="https://msdn.microsoft.com/c8c3b0c3-11b8-4123-91b6-75fed78932ce">gluNurbsProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>



<a href="https://msdn.microsoft.com/c8c3b0c3-11b8-4123-91b6-75fed78932ce">gluNurbsProperty</a>
 

 

