---
UID: NF:glu.gluGetTessProperty
title: gluGetTessProperty function
author: windows-driver-content
description: The gluGetTessProperty function gets a tessellation object property.
old-location: opengl\glugettessproperty.htm
old-project: OpenGL
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluGetTessProperty, glu/gluGetTessProperty, gluGetTessProperty, gluGetTessProperty function [OpenGL], opengl.glugettessproperty"
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
-	gluGetTessProperty
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluGetTessProperty function


## -description


The <b>gluGetTessProperty</b> function gets a tessellation object property.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param which

The property whose value is to be retrieved. The following values are valid: GLU_TESS_WINDING_RULE, GLU_TESS_BOUNDARY_ONLY, and GLU_TESS_TOLERANCE.


### -param value

A pointer to the location where the value of the named property is written.


## -returns



This function does not return a value.




## -remarks



Use <b>gluGetTessProperty</b> to retrieve properties stored in a tessellation object. These properties affect the way tessellation objects are interpreted and rendered. For information about what the properties are and what they do, see <a href="https://msdn.microsoft.com/1306b9ef-4f1e-4684-99ea-464bae1d0a61">gluTessProperty</a>.




## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/1306b9ef-4f1e-4684-99ea-464bae1d0a61">gluTessProperty</a>
 

 

