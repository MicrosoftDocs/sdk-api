---
UID: NF:wingdi.wglDeleteContext
title: wglDeleteContext function (wingdi.h)
description: The wglDeleteContext function deletes a specified OpenGL rendering context.
helpviewer_keywords: ["_ogl_wglDeleteContext","opengl.wgldeletecontext","wglDeleteContext","wglDeleteContext function [OpenGL]","wingdi/wglDeleteContext"]
old-location: opengl\wgldeletecontext.htm
tech.root: OpenGL
ms.assetid: 51d4cce1-fd2d-436e-816b-b89d3cd66f3a
ms.date: 12/05/2018
ms.keywords: _ogl_wglDeleteContext, opengl.wgldeletecontext, wglDeleteContext, wglDeleteContext function [OpenGL], wingdi/wglDeleteContext
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
 - wglDeleteContext
 - wingdi/wglDeleteContext
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
 - wglDeleteContext
---

# wglDeleteContext function


## -description

The <b>wglDeleteContext</b> function deletes a specified OpenGL rendering context.

## -parameters

### -param unnamedParam1

Handle to an OpenGL rendering context that the function will delete.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

It is an error to delete an OpenGL rendering context that is the current context of another thread. However, if a rendering context is the calling thread's current context, the <b>wglDeleteContext</b> function changes the rendering context to being not current before deleting it.

The <b>wglDeleteContext</b> function does not delete the device context associated with the OpenGL rendering context when you call the <b>wglMakeCurrent</b> function. After calling <b>wglDeleteContext</b>, you must call <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> to delete the associated device context.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext">wglGetCurrentContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc">wglGetCurrentDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent">wglMakeCurrent</a>