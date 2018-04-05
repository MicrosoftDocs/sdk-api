---
UID: NF:glu.gluUnProject
title: gluUnProject function
author: windows-driver-content
description: The gluUnProject function maps window coordinates to object coordinates.
old-location: opengl\gluunproject.htm
old-project: OpenGL
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluUnProject, glu/gluUnProject, gluUnProject, gluUnProject function [OpenGL], opengl.gluunproject"
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
-	gluUnProject
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluUnProject function


## -description


The <b>gluUnProject</b> function maps window coordinates to object coordinates.


## -parameters




### -param winx

The x window coordinate to be mapped.


### -param winy

The y window coordinate to be mapped.


### -param winz

The z window coordinate to be mapped.


### -param modelMatrix

The modelview matrix (as from a <a href="https://msdn.microsoft.com/9d99e653-7997-4e38-82d2-e7b1525208fe">glGetDoublev</a> call).


### -param projMatrix

The projection matrix (as from a <b>glGetDoublev</b> call).


### -param viewport

The viewport (as from a <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetIntegerv</a> call).


### -param objx

The computed x object coordinate.


### -param objy

The computed y object coordinate.


### -param objz

The computed z object coordinate.


## -returns



If the function succeeds, the return value is GL_TRUE.

If the function fails, the return value is GL_FALSE.




## -remarks



The <b>gluUnProject</b> function maps the specified window coordinates into object coordinates using <i>modelMatrix</i>, <i>projMatrix</i>, and <i>viewport</i>. The result is stored in <i>objx</i>, <i>objy</i>, and <i>objz</i>.




## -see-also




<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetDoublev</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetIntegerv</a>



<a href="https://msdn.microsoft.com/cfd8bc5b-b684-4207-8bdb-bf086858da13">gluProject</a>
 

 

