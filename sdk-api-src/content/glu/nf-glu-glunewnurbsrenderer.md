---
UID: NF:glu.gluNewNurbsRenderer
title: gluNewNurbsRenderer function
author: windows-driver-content
description: The gluNewNurbsRenderer function creates a Non-Uniform Rational B-Spline (NURBS) object.
old-location: opengl\glunewnurbsrenderer.htm
old-project: OpenGL
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluNewNurbsRenderer, glu/gluNewNurbsRenderer, gluNewNurbsRenderer, gluNewNurbsRenderer function [OpenGL], opengl.glunewnurbsrenderer"
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
-	gluNewNurbsRenderer
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNewNurbsRenderer function


## -description


The <b>gluNewNurbsRenderer</b> function creates a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) object.


## -parameters






## -remarks



The <b>gluNewNurbsRenderer</b> function creates and returns a pointer to a new NURBS object. Refer to this object when calling NURBS rendering and control functions. A return value of zero means there is not enough memory to allocate to the object.




## -see-also




<a href="https://msdn.microsoft.com/f7f2e765-1a07-4faa-940c-9cb957dd54d4">gluBeginCurve</a>



<a href="https://msdn.microsoft.com/7189f05e-0c4d-4f82-8a82-a51fcc51b202">gluBeginSurface</a>



<a href="https://msdn.microsoft.com/636402d0-8f6d-4ad8-84c6-66364025d788">gluBeginTrim</a>



<a href="https://msdn.microsoft.com/77063dcb-90b8-47e4-8b00-e1c46cf4f712">gluDeleteNurbsRenderer</a>



<a href="https://msdn.microsoft.com/1e9afc00-57c6-459e-a9fc-463f45df2084">gluNurbsCallback</a>



<a href="https://msdn.microsoft.com/c8c3b0c3-11b8-4123-91b6-75fed78932ce">gluNurbsProperty</a>
 

 

