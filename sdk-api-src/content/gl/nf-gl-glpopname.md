---
UID: NF:gl.glPopName
title: glPopName function
author: windows-driver-content
description: The glPushName and glPopName functions push and pop the name stack.
old-location: opengl\glpopname.htm
old-project: OpenGL
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPopName, glPopName, glPopName function [OpenGL], opengl.glpopname
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
-	glPopName
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPopName function


## -description


The <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a> and <b>glPopName</b> functions push and pop the name stack.


## -parameters






## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a> function causes name to be pushed onto the name stack, which is initially empty. The <b>glPopName</b> function pops one name off the top of the stack. The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified. It consists of an ordered set of unsigned integers. 

The name stack is always empty while the render mode is not GL_SELECT. Calls to <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a> or <b>glPopName</b> while the render mode is not GL_SELECT are ignored.

The following functions retrieve information related to <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a> and <b>glPopName</b>:



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_NAME_STACK_DEPTH



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAX_NAME_STACK_DEPTH





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/26c134f5-c17c-4637-93b6-5293f316dd6c">glInitNames</a>



<a href="https://msdn.microsoft.com/8d7d582b-3743-401e-af71-28034e49f3c2">glLoadName</a>



<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>



<a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a>
 

 

