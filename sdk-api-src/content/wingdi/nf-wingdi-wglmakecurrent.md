---
UID: NF:wingdi.wglMakeCurrent
title: wglMakeCurrent function (wingdi.h)
description: The wglMakeCurrent function makes a specified OpenGL rendering context the calling thread's current rendering context.
helpviewer_keywords: ["_ogl_wglMakeCurrent","opengl.wglmakecurrent","wglMakeCurrent","wglMakeCurrent function [OpenGL]","wingdi/wglMakeCurrent"]
old-location: opengl\wglmakecurrent.htm
tech.root: OpenGL
ms.assetid: a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe
ms.date: 12/05/2018
ms.keywords: _ogl_wglMakeCurrent, opengl.wglmakecurrent, wglMakeCurrent, wglMakeCurrent function [OpenGL], wingdi/wglMakeCurrent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wglMakeCurrent
 - wingdi/wglMakeCurrent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglMakeCurrent
---

# wglMakeCurrent function


## -description

The <b>wglMakeCurrent</b> function makes a specified OpenGL rendering context the calling thread's current rendering context. All subsequent OpenGL calls made by the thread are drawn on the device identified by <i>hdc</i>. You can also use <b>wglMakeCurrent</b> to change the calling thread's current rendering context so it's no longer current.

## -parameters

### -param unnamedParam1

Handle to a device context. Subsequent OpenGL calls made by the calling thread are drawn on the device identified by <i>hdc</i>.

### -param unnamedParam2

Handle to an OpenGL rendering context that the function sets as the calling thread's rendering context.

If <i>hglrc</i> is <b>NULL</b>, the function makes the calling thread's current rendering context no longer current, and releases the device context that is used by the rendering context. In this case, <i>hdc</i> is ignored.

## -returns

When the <b>wglMakeCurrent</b> function succeeds, the return value is <b>TRUE</b>; otherwise the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <i>hdc</i> parameter must refer to a drawing surface supported by OpenGL. It need not be the same <i>hdc</i> that was passed to <a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a> when <i>hglrc</i> was created, but it must be on the same device and have the same pixel format. GDI transformation and clipping in <i>hdc</i> are not supported by the rendering context. The current rendering context uses the <i>hdc</i> device context until the rendering context is no longer current.

Before switching to the new rendering context, OpenGL flushes any previous rendering context that was current to the calling thread.

A thread can have one current rendering context. A process can have multiple rendering contexts by means of multithreading. A thread must set a current rendering context before calling any OpenGL functions. Otherwise, all OpenGL calls are ignored.

A rendering context can be current to only one thread at a time. You cannot make a rendering context current to multiple threads.

An application can perform multithread drawing by making different rendering contexts current to different threads, supplying each thread with its own rendering context and device context.

If an error occurs, the <b>wglMakeCurrent</b> function makes the thread's current rendering context not current before returning.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext">wglGetCurrentContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc">wglGetCurrentDC</a>