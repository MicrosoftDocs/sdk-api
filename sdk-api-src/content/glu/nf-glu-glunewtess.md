---
UID: NF:glu.gluNewTess
title: gluNewTess function
author: windows-driver-content
description: The gluNewTess function creates a tessellation object.
old-location: opengl\glunewtess.htm
old-project: OpenGL
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluNewTess, glu/gluNewTess, gluNewTess, gluNewTess function [OpenGL], opengl.glunewtess"
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
-	gluNewTess
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNewTess function


## -description


The <b>gluNewTess</b> function creates a tessellation object.


## -parameters






## -remarks



The <b>gluNewTess</b> function creates and returns a pointer to a new tessellation object. Refer to this object when calling tessellation functions. A return value of zero means there is not enough memory to allocate to the object.




## -see-also




<a href="https://msdn.microsoft.com/7e1540f7-5e7d-4a3b-8c94-5a6800b17411">gluDeleteTess</a>



<a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>
 

 

