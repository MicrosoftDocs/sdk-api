---
UID: NF:wingdi.wglCreateLayerContext
title: wglCreateLayerContext function
author: windows-driver-content
description: The wglCreateLayerContext function creates a new OpenGL rendering context for drawing to a specified layer plane on a device context.
old-location: opengl\wglcreatelayercontext.htm
old-project: OpenGL
ms.assetid: 81050b48-7385-4ef3-acc5-82d5c893b2e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_wglCreateLayerContext, opengl.wglcreatelayercontext, wglCreateLayerContext, wglCreateLayerContext function [OpenGL], wingdi/wglCreateLayerContext"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	wglCreateLayerContext
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wglCreateLayerContext function


## -description


The <b>wglCreateLayerContext</b> function creates a new OpenGL rendering context for drawing to a specified layer plane on a device context.


## -parameters




### -param

TBD




#### - hdc

Specifies the device context for a new rendering context.


#### - iLayerPlane

Specifies the layer plane to which you want to bind a rendering context. The value 0 identifies the main plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure.


## -returns



If the function succeeds, the return value is a handle to an OpenGL rendering context.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A rendering context is a port through which all OpenGL commands pass. Every thread that makes OpenGL calls must have one current, active rendering context. A rendering context is not the same as a device context; a rendering context contains information specific to OpenGL, while a device context contains information specific to GDI.

Before you create a rendering context, set the pixel format of the device context with the <a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a> function. You can use a rendering context in a specified layer plane of a window with identical pixel formats only.

With OpenGL applications that use multiple threads, you create a rendering context, select it as the current rendering context of a thread, and make OpenGL calls for the specified thread. When you are finished with the rendering context of the thread, call the <a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a> function. 


#### Examples

The following code example shows how to use <b>wglCreateLayerContext</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The following code fragment shows how to render to overlay 1  
// This example assumes that the pixel format of hdc includes   
// overlay plane 1  
 
HDC hdc; 
HGLRC; 
 
// create a rendering context for overlay plane 1  
hglrc = wglCreateLayerContext(hdc, 1); 
 
// make it the calling thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// call OpenGL functions here. . .  
 
// when the rendering context is no longer needed. . .  
 
// make the rendering context not current  
wglMakeCurrent(NULL, NULL); 
 
// delete the rendering context  
wglDeleteContext(hglrc);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a>



<a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a>



<a href="https://msdn.microsoft.com/8e2a4f24-689c-48b7-a06e-fc57d65b5567">wglGetCurrentContext</a>



<a href="https://msdn.microsoft.com/026f6181-75a2-4781-8762-d5599ce90af2">wglGetCurrentDC</a>



<a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>
 

 

