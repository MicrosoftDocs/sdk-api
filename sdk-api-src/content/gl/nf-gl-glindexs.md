---
UID: NF:gl.glIndexs
title: glIndexs function
author: windows-driver-content
description: The glIndexs function sets the current color index.
old-location: opengl\glindexs.htm
old-project: OpenGL
ms.assetid: 193304e6-c88a-49a6-935b-29bcf1954564
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glIndexs, glIndexs, glIndexs function [OpenGL], opengl.glindexs
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
-	glIndexs
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glIndexs function


## -description


The <b>glIndexs</b> function sets the current color index.


## -parameters




### -param c

The new value for the current color index.


## -returns



This function does not return a value.




## -remarks



The <b>glIndexs</b> function updates the current (single-valued) color index. It takes one argument: the new value for the current color index.


The current index is stored as a floating-point value. Integer values are converted directly to floating-point values, with no special mapping.

Index values outside the representable range of the color-index buffer are not clamped. However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format. Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.

The current index can be updated at any time. In particular, <b>glIndexs</b> can be called between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>.


The following function retrieves information related to <b>glIndexs</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_CURRENT_INDEX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
 

 

