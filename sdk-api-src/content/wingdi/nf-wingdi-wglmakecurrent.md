---
UID: NF:wingdi.wglMakeCurrent
title: wglMakeCurrent function
author: windows-sdk-content
description: The wglMakeCurrent function makes a specified OpenGL rendering context the calling thread's current rendering context.
old-location: opengl\wglmakecurrent.htm
tech.root: OpenGL
ms.assetid: a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ogl_wglMakeCurrent, opengl.wglmakecurrent, wglMakeCurrent, wglMakeCurrent function [OpenGL], wingdi/wglMakeCurrent"
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
 - wglMakeCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- wglMakeCurrent
: 
---

# wglMakeCurrent function


## -description


The <b>wglMakeCurrent</b> function makes a specified OpenGL rendering context the calling thread's current rendering context. All subsequent OpenGL calls made by the thread are drawn on the device identified by <i>hdc</i>. You can also use <b>wglMakeCurrent</b> to change the calling thread's current rendering context so it's no longer current.


## -parameters




### -param arg1

Handle to a device context. Subsequent OpenGL calls made by the calling thread are drawn on the device identified by <i>hdc</i>.


### -param arg2

Handle to an OpenGL rendering context that the function sets as the calling thread's rendering context.

If <i>hglrc</i> is <b>NULL</b>, the function makes the calling thread's current rendering context no longer current, and releases the device context that is used by the rendering context. In this case, <i>hdc</i> is ignored.


## -returns



When the <b>wglMakeCurrent</b> function succeeds, the return value is <b>TRUE</b>; otherwise the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <i>hdc</i> parameter must refer to a drawing surface supported by OpenGL. It need not be the same <i>hdc</i> that was passed to <a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a> when <i>hglrc</i> was created, but it must be on the same device and have the same pixel format. GDI transformation and clipping in <i>hdc</i> are not supported by the rendering context. The current rendering context uses the <i>hdc</i> device context until the rendering context is no longer current.

Before switching to the new rendering context, OpenGL flushes any previous rendering context that was current to the calling thread.

A thread can have one current rendering context. A process can have multiple rendering contexts by means of multithreading. A thread must set a current rendering context before calling any OpenGL functions. Otherwise, all OpenGL calls are ignored.

A rendering context can be current to only one thread at a time. You cannot make a rendering context current to multiple threads.

An application can perform multithread drawing by making different rendering contexts current to different threads, supplying each thread with its own rendering context and device context.

If an error occurs, the <b>wglMakeCurrent</b> function makes the thread's current rendering context not current before returning.




## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a>



<a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a>



<a href="https://msdn.microsoft.com/8e2a4f24-689c-48b7-a06e-fc57d65b5567">wglGetCurrentContext</a>



<a href="https://msdn.microsoft.com/026f6181-75a2-4781-8762-d5599ce90af2">wglGetCurrentDC</a>
 

 

