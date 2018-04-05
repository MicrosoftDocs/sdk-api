---
UID: NF:glu.gluDeleteTess
title: gluDeleteTess function
author: windows-driver-content
description: The gluDeleteTess function destroys a tessellation object.
old-location: opengl\gludeletetess.htm
old-project: OpenGL
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluDeleteTess, glu/gluDeleteTess, gluDeleteTess, gluDeleteTess function [OpenGL], opengl.gludeletetess"
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
-	gluDeleteTess
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluDeleteTess function


## -description


The <b>gluDeleteTess</b> function destroys a tessellation object.


## -parameters




### -param tess

The tessellation object to destroy (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


## -returns



This function does not return a value.




## -remarks



The <b>gluDeleteTess</b> function destroys the indicated tessellation object and frees any memory that it used.




## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>
 

 

