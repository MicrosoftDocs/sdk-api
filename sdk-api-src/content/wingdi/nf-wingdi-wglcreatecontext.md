---
UID: NF:wingdi.wglCreateContext
title: wglCreateContext function (wingdi.h)
description: The wglCreateContext function creates a new OpenGL rendering context, which is suitable for drawing on the device referenced by hdc. The rendering context has the same pixel format as the device context.
helpviewer_keywords: ["_ogl_wglCreateContext","opengl.wglcreatecontext","wglCreateContext","wglCreateContext function [OpenGL]","wingdi/wglCreateContext"]
old-location: opengl\wglcreatecontext.htm
tech.root: OpenGL
ms.assetid: fa9ed944-f917-4fdf-a52a-10a7ade8f2ca
ms.date: 12/05/2018
ms.keywords: _ogl_wglCreateContext, opengl.wglcreatecontext, wglCreateContext, wglCreateContext function [OpenGL], wingdi/wglCreateContext
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
 - wglCreateContext
 - wingdi/wglCreateContext
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
 - wglCreateContext
---

# wglCreateContext function

## -description

The <b>wglCreateContext</b> function creates a new OpenGL rendering context, which is suitable for drawing on the device referenced by <i>hdc</i>. The rendering context has the same pixel format as the device context.

## -parameters

### -param unnamedParam1

Typically named `handleToDeviceContext`. Handle to a device context for which the function creates a suitable OpenGL rendering context.

## -returns

If the function succeeds, the return value is a valid handle to an OpenGL rendering context.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A rendering context is not the same as a device context. Set the pixel format of the device context before creating a rendering context. For more information on setting the device context's pixel format, see the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a> function.

To use OpenGL, you create a rendering context, select it as a thread's current rendering context, and then call OpenGL functions. When you are finished with the rendering context, you dispose of it by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a> function.

The following code example shows <b>wglCreateContext</b> usage.


``` syntax
HDC    hdc; 
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
wglDeleteContext (hglrc);
```


## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext">wglGetCurrentContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc">wglGetCurrentDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent">wglMakeCurrent</a>
