---
UID: NF:glu.gluNurbsCallback
title: gluNurbsCallback function
author: windows-driver-content
description: The gluNurbsCallback function defines a callback for a Non-Uniform Rational B-Spline (NURBS) object.
old-location: opengl\glunurbs.htm
old-project: OpenGL
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluNurbsCallback, glu/gluNurbsCallback, gluNurbsCallback, gluNurbsCallback function [OpenGL], opengl.glunurbs"
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
-	gluNurbsCallback
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNurbsCallback function


## -description


The <b>gluNurbsCallback</b> function defines a callback for a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) object.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param which

The callback being defined. The only valid value is GLU_ERROR. The meaning of GLU_ERROR means that the error function is called when an error is encountered. Its single argument is of type <b>GLenum</b>, and it indicates the specific error that occurred. There are 37 errors unique to NURBS, named GLU_NURBS_ERROR1 through GLU_NURBS_ERROR37. Character strings describing these errors can be retrieved with <a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>.


### -param fn

A pointer to the callback function.


## -returns



This function does not return a value.




## -remarks



Use <b>gluNurbsCallback</b> to define a callback to be used by a NURBS object. If the specified callback is already defined, it is replaced. If <i>fn</i> is <b>NULL</b>, then any existing callback is erased.




## -see-also




<a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>
 

 

