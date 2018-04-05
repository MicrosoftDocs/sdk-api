---
UID: NF:gl.glGenLists
title: glGenLists function
author: windows-driver-content
description: The glGenLists function generates a contiguous set of empty display lists.
old-location: opengl\glgenlists.htm
old-project: OpenGL
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGenLists, gl/glGenLists, glGenLists, glGenLists function [OpenGL], opengl.glgenlists"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
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
-	opengl32.dll
api_name:
-	glGenLists
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGenLists function


## -description


The <b>glGenLists</b> function generates a contiguous set of empty display lists.


## -parameters




### -param range

The number of contiguous empty display lists to be generated.


## -remarks



The <b>glGenLists</b> function has one argument, <i>range</i>. It returns an integer <i>n</i> such that <i>range</i> contiguous empty display lists, named <i>n</i>, <i>n</i> + 1, . . ., <i>n</i> + (<i>range</i> - 1), are created. If <i>range</i> is zero, if there is no group of <i>range</i> contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.

The following function retrieves information related to <b>glGenLists</b>:


<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/979ab352-99db-4822-922c-a1813b9fcfce">glDeleteLists</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>
 

 

