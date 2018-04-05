---
UID: NF:glu.gluOrtho2D
title: gluOrtho2D function
author: windows-driver-content
description: The gluOrtho2D function defines a 2-D orthographic projection matrix.
old-location: opengl\gluortho2d.htm
old-project: OpenGL
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluOrtho2D, glu/gluOrtho2D, gluOrtho2D, gluOrtho2D function [OpenGL], opengl.gluortho2d"
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
-	gluOrtho2D
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluOrtho2D function


## -description


The <b>gluOrtho2D</b> function defines a 2-D orthographic projection matrix.


## -parameters




### -param left

The coordinate for the left vertical clipping plane.


### -param right

The coordinate for the right vertical clipping plane.


### -param bottom

The coordinate for the bottom horizontal clipping plane.


### -param top

The coordinate for the top horizontal clipping plane.


## -returns



This function does not return a value.




## -remarks



The <b>gluOrtho2D</b> function sets up a two-dimensional orthographic viewing region. This is equivalent to calling <a href="https://msdn.microsoft.com/5c70819f-e9b6-49e2-add5-9f6e6aba26ee">glOrtho</a> with near = –1 and far = 1.




## -see-also




<a href="https://msdn.microsoft.com/5c70819f-e9b6-49e2-add5-9f6e6aba26ee">glOrtho</a>



<a href="https://msdn.microsoft.com/125e2828-a2d7-4c6c-9370-eb21a581ced8">gluPerspective</a>
 

 

