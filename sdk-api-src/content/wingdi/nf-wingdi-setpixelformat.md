---
UID: NF:wingdi.SetPixelFormat
title: SetPixelFormat function (wingdi.h)
description: The SetPixelFormat function sets the pixel format of the specified device context to the format specified by the iPixelFormat index.
helpviewer_keywords: ["SetPixelFormat","SetPixelFormat function [OpenGL]","_ogl_SetPixelFormat","opengl.setpixelformat","wingdi/SetPixelFormat"]
old-location: opengl\setpixelformat.htm
tech.root: OpenGL
ms.assetid: f8d74078-a7e7-4d95-857a-f51d5d70598e
ms.date: 12/05/2018
ms.keywords: SetPixelFormat, SetPixelFormat function [OpenGL], _ogl_SetPixelFormat, opengl.setpixelformat, wingdi/SetPixelFormat
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetPixelFormat
 - wingdi/SetPixelFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetPixelFormat
---

# SetPixelFormat function


## -description

The <b>SetPixelFormat</b> function sets the pixel format of the specified device context to the format specified by the <i>iPixelFormat</i> index.

## -parameters

### -param hdc

Specifies the device context whose pixel format the function attempts to set.

### -param format

Index that identifies the pixel format to set. The various pixel formats supported by a device context are identified by one-based indexes.

### -param ppfd

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure that contains the logical pixel format specification. The system's metafile component uses this structure to record the logical pixel format specification. The structure has no other effect upon the behavior of the <b>SetPixelFormat</b> function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>hdc</i> references a window, calling the <b>SetPixelFormat</b> function also changes the pixel format of the window. Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed. An application can only set the pixel format of a window one time. Once a window's pixel format is set, it cannot be changed.

You should select a pixel format in the device context before calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a> function. The <b>wglCreateContext</b> function creates a rendering context for drawing on the device in the selected pixel format of the device context.

An OpenGL window has its own pixel format. Because of this, only device contexts retrieved for the client area of an OpenGL window are allowed to draw into the window. As a result, an OpenGL window should be created with the WS_CLIPCHILDREN and WS_CLIPSIBLINGS styles. Additionally, the window class attribute should not include the CS_PARENTDC style.


#### Examples

The following code example shows <b>SetPixelFormat</b> usage.


```cpp
PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),   // size of this pfd  
    1,                     // version number  
    PFD_DRAW_TO_WINDOW |   // support window  
    PFD_SUPPORT_OPENGL |   // support OpenGL  
    PFD_DOUBLEBUFFER,      // double buffered  
    PFD_TYPE_RGBA,         // RGBA type  
    24,                    // 24-bit color depth  
    0, 0, 0, 0, 0, 0,      // color bits ignored  
    0,                     // no alpha buffer  
    0,                     // shift bit ignored  
    0,                     // no accumulation buffer  
    0, 0, 0, 0,            // accum bits ignored  
    32,                    // 32-bit z-buffer  
    0,                     // no stencil buffer  
    0,                     // no auxiliary buffer  
    PFD_MAIN_PLANE,        // main layer  
    0,                     // reserved  
    0, 0, 0                // layer masks ignored  
}; 
HDC  hdc; 
int  iPixelFormat; 
 
// get the best available match of pixel format for the device context   
iPixelFormat = ChoosePixelFormat(hdc, &pfd); 
 
// make that the pixel format of the device context  
SetPixelFormat(hdc, iPixelFormat, &pfd);
```

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat">ChoosePixelFormat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-describepixelformat">DescribePixelFormat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpixelformat">GetPixelFormat</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/win32-functions">Windows Functions</a>