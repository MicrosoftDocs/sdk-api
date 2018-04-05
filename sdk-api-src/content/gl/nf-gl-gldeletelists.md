---
UID: NF:gl.glDeleteLists
title: glDeleteLists function
author: windows-driver-content
description: The glDeleteLists function deletes a contiguous group of display lists.
old-location: opengl\gldeletelists.htm
old-project: OpenGL
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glDeleteLists, gl/glDeleteLists, glDeleteLists, glDeleteLists function [OpenGL], opengl.gldeletelists"
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
-	glDeleteLists
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDeleteLists function


## -description


The <b>glDeleteLists</b> function deletes a contiguous group of display lists.


## -parameters




### -param list

The integer name of the first display list to delete.


### -param range

The number of display lists to delete.


## -returns



This function does not return a value.




## -remarks



The <b>glDeleteLists</b> function causes a contiguous group of display lists to be deleted. The <i>list</i> parameter is the name of the first display list to be deleted, and <i>range</i> is the number of display lists to delete. All display lists <i>d</i> with <i>list</i> ≤ <i>d</i> ≤ <i>list</i> + <i>range</i> - 1 are deleted.

All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time. Names within the range that do not have an associated display list are ignored. If <i>range</i> is zero, nothing happens.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a>



<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>
 

 

