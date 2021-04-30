---
UID: NF:wingdi.wglCreateLayerContext
title: wglCreateLayerContext function (wingdi.h)
description: The wglCreateLayerContext function creates a new OpenGL rendering context for drawing to a specified layer plane on a device context.
helpviewer_keywords: ["_ogl_wglCreateLayerContext","opengl.wglcreatelayercontext","wglCreateLayerContext","wglCreateLayerContext function [OpenGL]","wingdi/wglCreateLayerContext"]
old-location: opengl\wglcreatelayercontext.htm
tech.root: OpenGL
ms.assetid: 81050b48-7385-4ef3-acc5-82d5c893b2e8
ms.date: 12/05/2018
ms.keywords: _ogl_wglCreateLayerContext, opengl.wglcreatelayercontext, wglCreateLayerContext, wglCreateLayerContext function [OpenGL], wingdi/wglCreateLayerContext
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
 - wglCreateLayerContext
 - wingdi/wglCreateLayerContext
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
 - wglCreateLayerContext
---

# wglCreateLayerContext function


## -description

The <b>wglCreateLayerContext</b> function creates a new OpenGL rendering context for drawing to a specified layer plane on a device context.

## -parameters

### -param unnamedParam1

Specifies the device context for a new rendering context.

### -param unnamedParam2

Specifies the layer plane to which you want to bind a rendering context. The value 0 identifies the main plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure.

## -returns

If the function succeeds, the return value is a handle to an OpenGL rendering context.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A rendering context is a port through which all OpenGL commands pass. Every thread that makes OpenGL calls must have one current, active rendering context. A rendering context is not the same as a device context; a rendering context contains information specific to OpenGL, while a device context contains information specific to GDI.

Before you create a rendering context, set the pixel format of the device context with the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a> function. You can use a rendering context in a specified layer plane of a window with identical pixel formats only.

With OpenGL applications that use multiple threads, you create a rendering context, select it as the current rendering context of a thread, and make OpenGL calls for the specified thread. When you are finished with the rendering context of the thread, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a> function. 


#### Examples

The following code example shows how to use <b>wglCreateLayerContext</b>.


```cpp
// The following code fragment shows how to render to overlay 1  
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
wglDeleteContext(hglrc);
```

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext">wglGetCurrentContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc">wglGetCurrentDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent">wglMakeCurrent</a>