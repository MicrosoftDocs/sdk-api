---
UID: NF:glu.gluDeleteNurbsRenderer
title: gluDeleteNurbsRenderer function
author: windows-driver-content
description: The gluDeleteNurbsRenderer function destroys a Non-Uniform Rational B-Spline (NURBS) object.
old-location: opengl\gludeletenurbsrenderer.htm
old-project: OpenGL
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluDeleteNurbsRenderer, glu/gluDeleteNurbsRenderer, gluDeleteNurbsRenderer, gluDeleteNurbsRenderer function [OpenGL], opengl.gludeletenurbsrenderer"
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
-	gluDeleteNurbsRenderer
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluDeleteNurbsRenderer function


## -description


The <b>gluDeleteNurbsRenderer</b> function destroys a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) object.


## -parameters




### -param nobj

The NURBS object to be destroyed (created with <b>gluNewNurbsRenderer</b>).


## -returns



This function does not return a value.




## -remarks



The <b>gluDeleteNurbsRenderer</b> function destroys the NURBS object and frees any memory that it used. After you have called <b>gluDeleteNurbsRenderer</b>, you cannot use <i>nobj</i> again.




## -see-also




<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>
 

 

