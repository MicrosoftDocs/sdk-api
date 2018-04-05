---
UID: NF:glu.gluProject
title: gluProject function
author: windows-driver-content
description: The gluProject function maps object coordinates to window coordinates.
old-location: opengl\gluproject.htm
old-project: OpenGL
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluProject, glu/gluProject, gluProject, gluProject function [OpenGL], opengl.gluproject"
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
-	gluProject
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluProject function


## -description


The <b>gluProject</b> function maps object coordinates to window coordinates.


## -parameters




### -param objx

The x object coordinate.


### -param objy

The y object coordinate.


### -param objz

The z object coordinate.


### -param modelMatrix

The current modelview matrix (as from a <a href="https://msdn.microsoft.com/9d99e653-7997-4e38-82d2-e7b1525208fe">glGetDoublev</a> call).


### -param projMatrix

The current projection matrix (as from a <b>glGetDoublev</b> call).


### -param viewport

The current viewport (as from a <a href="https://msdn.microsoft.com/16b04af6-5da3-439f-8d4f-bc8ab1fcb2c5">glGetIntegerv</a> call).


### -param winx

The computed x window coordinate.


### -param winy

The computed y window coordinate.


### -param winz

The computed z window coordinate.


## -returns



If the function succeeds, the return value is GL_TRUE.

If the function fails, the return value is GL_FALSE.




## -remarks



The <b>gluProject</b> function transforms the specified object coordinates into window coordinates using <i>modelMatrix</i>, <i>projMatrix</i>, and <i>viewport</i>. The result is stored in <i>winx</i>, <i>winy</i>, and <i>winz</i>.




## -see-also




<a href="https://msdn.microsoft.com/9d99e653-7997-4e38-82d2-e7b1525208fe">glGetDoublev</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetIntegerv</a>



<a href="https://msdn.microsoft.com/6a719fc2-ad40-4b22-9c99-5753f5dbb8a0">gluUnProject</a>
 

 

