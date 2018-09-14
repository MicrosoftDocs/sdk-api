---
UID: NF:wingdi.wglCreateContext
title: wglCreateContext function
author: windows-sdk-content
description: The wglCreateContext function creates a new OpenGL rendering context, which is suitable for drawing on the device referenced by hdc. The rendering context has the same pixel format as the device context.
old-location: opengl\wglcreatecontext.htm
tech.root: OpenGL
ms.assetid: fa9ed944-f917-4fdf-a52a-10a7ade8f2ca
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_ogl_wglCreateContext, opengl.wglcreatecontext, wglCreateContext, wglCreateContext function [OpenGL], wingdi/wglCreateContext"
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
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglCreateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# wglCreateContext function


## -description


The <b>wglCreateContext</b> function creates a new OpenGL rendering context, which is suitable for drawing on the device referenced by <i>hdc</i>. The rendering context has the same pixel format as the device context.


## -parameters




### -param Arg1

Handle to a device context for which the function creates a suitable OpenGL rendering context.


## -returns



If the function succeeds, the return value is a valid handle to an OpenGL rendering context.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A rendering context is not the same as a device context. Set the pixel format of the device context before creating a rendering context. For more information on setting the device context's pixel format, see the <a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a> function.

To use OpenGL, you create a rendering context, select it as a thread's current rendering context, and then call OpenGL functions. When you are finished with the rendering context, you dispose of it by calling the <a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a> function.

The following code example shows <b>wglCreateContext</b> usage.

<pre class="syntax" xml:space="preserve"><code>HDC    hdc; 
HGLRC  hglrc; 
 
// create a rendering context  
hglrc = wglCreateContext (hdc); 
 
// make it the calling thread's current rendering context 
wglMakeCurrent (hdc, hglrc);
 
// call OpenGL APIs as desired ... 
 
// when the rendering context is no longer needed ...   
 
// make the rendering context not current  
wglMakeCurrent (NULL, NULL) ; 
 
// delete the rendering context  
wglDeleteContext (hglrc);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a>



<a href="https://msdn.microsoft.com/8e2a4f24-689c-48b7-a06e-fc57d65b5567">wglGetCurrentContext</a>



<a href="https://msdn.microsoft.com/026f6181-75a2-4781-8762-d5599ce90af2">wglGetCurrentDC</a>



<a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>
 

 

