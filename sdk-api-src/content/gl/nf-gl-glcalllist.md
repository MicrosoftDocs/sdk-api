---
UID: NF:gl.glCallList
title: glCallList function
author: windows-driver-content
description: The glCallList function executes a display list.
old-location: opengl\glcalllist.htm
old-project: OpenGL
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glCallList, gl/glCallList, glCallList, glCallList function [OpenGL], opengl.glcalllist"
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
-	glCallList
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glCallList function


## -description


The <b>glCallList</b> function executes a display list.


## -parameters




### -param list

The integer name of the display list to be executed.


## -returns



This function does not return a value.




## -remarks



Invoking the <b>glCallList</b> function begins execution of the named display list. The functions saved in the display list are executed in order, just as if you called them without using a display list. If <i>list</i> has not been defined as a display list, <b>glCallList</b> is ignored.

The <b>glCallList</b> function can appear inside a display list. To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution. This limit is at least 64, however, it depends on the implementation.

The OpenGL state is not saved and restored across a call to <b>glCallList</b>. Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed. To preserve the OpenGL state across <b>glCallList</b> calls, use <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>, <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>, <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>, and <a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a>.

You can execute display lists between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>, as long as the display list includes only functions that are allowed in this interval.

The following functions retrieve information related to <b>glCallList</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAX_LIST_NESTING


<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/979ab352-99db-4822-922c-a1813b9fcfce">glDeleteLists</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>



<a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>



<a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>
 

 

