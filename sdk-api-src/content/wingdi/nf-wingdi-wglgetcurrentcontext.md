---
UID: NF:wingdi.wglGetCurrentContext
title: wglGetCurrentContext function (wingdi.h)
description: The wglGetCurrentContext function obtains a handle to the current OpenGL rendering context of the calling thread.
helpviewer_keywords: ["_ogl_wglGetCurrentContext","opengl.wglgetcurrentcontext","wglGetCurrentContext","wglGetCurrentContext function [OpenGL]","wingdi/wglGetCurrentContext"]
old-location: opengl\wglgetcurrentcontext.htm
tech.root: OpenGL
ms.assetid: 8e2a4f24-689c-48b7-a06e-fc57d65b5567
ms.date: 12/05/2018
ms.keywords: _ogl_wglGetCurrentContext, opengl.wglgetcurrentcontext, wglGetCurrentContext, wglGetCurrentContext function [OpenGL], wingdi/wglGetCurrentContext
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
 - wglGetCurrentContext
 - wingdi/wglGetCurrentContext
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
 - wglGetCurrentContext
---

# wglGetCurrentContext function


## -description

The <b>wglGetCurrentContext</b> function obtains a handle to the current OpenGL rendering context of the calling thread.



## -returns

If the calling thread has a current OpenGL rendering context, <b>wglGetCurrentContext</b> returns a handle to that rendering context. Otherwise, the return value is <b>NULL</b>.

## -remarks

The current OpenGL rendering context of a thread is associated with a device context by means of the <b>wglMakeCurrent</b> function. You can use the <b>wglGetCurrentDC</b> function to obtain a handle to the device context associated with the current OpenGL rendering context.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc">wglGetCurrentDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent">wglMakeCurrent</a>
