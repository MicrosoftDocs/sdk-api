---
UID: NF:glu.gluDeleteQuadric
title: gluDeleteQuadric function
author: windows-driver-content
description: The gluDeleteQuadric function destroys a quadric object.
old-location: opengl\gludeletequadric.htm
old-project: OpenGL
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluDeleteQuadric, glu/gluDeleteQuadric, gluDeleteQuadric, gluDeleteQuadric function [OpenGL], opengl.gludeletequadric"
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
-	gluDeleteQuadric
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluDeleteQuadric function


## -description


The <b>gluDeleteQuadric</b> function destroys a quadric object.


## -parameters




### -param state

The quadric object to be destroyed (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


## -returns



This function does not return a value.




## -remarks



The <b>gluDeleteQuadric</b> function destroys the quadric object and frees any memory that it used. After you have called <b>gluDeleteQuadric</b>, you cannot use <i>state</i> again.




## -see-also




<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>
 

 

