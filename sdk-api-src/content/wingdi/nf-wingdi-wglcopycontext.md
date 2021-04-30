---
UID: NF:wingdi.wglCopyContext
title: wglCopyContext function (wingdi.h)
description: The wglCopyContext function copies selected groups of rendering states from one OpenGL rendering context to another.
helpviewer_keywords: ["_ogl_wglCopyContext","opengl.wglcopycontext","wglCopyContext","wglCopyContext function [OpenGL]","wingdi/wglCopyContext"]
old-location: opengl\wglcopycontext.htm
tech.root: OpenGL
ms.assetid: dc350848-7921-41b8-96f1-c0eabad3d157
ms.date: 12/05/2018
ms.keywords: _ogl_wglCopyContext, opengl.wglcopycontext, wglCopyContext, wglCopyContext function [OpenGL], wingdi/wglCopyContext
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
 - wglCopyContext
 - wingdi/wglCopyContext
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
 - wglCopyContext
---

# wglCopyContext function


## -description

The <b>wglCopyContext</b> function copies selected groups of rendering states from one OpenGL rendering context to another.

## -parameters

### -param unnamedParam1

Specifies the source OpenGL rendering context whose state information is to be copied.

### -param unnamedParam2

Specifies the destination OpenGL rendering context to which state information is to be copied.

### -param unnamedParam3

Specifies which groups of the <i>hglrcSrc</i> rendering state are to be copied to <i>hglrcDst</i>. It contains the bitwise-OR of the same symbolic names that are passed to the <b>glPushAttrib</b> function. You can use GL_ALL_ATTRIB_BITS to copy all the rendering state information.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Using the <b>wglCopyContext</b> function, you can synchronize the rendering state of two rendering contexts. You can only copy the rendering state between two rendering contexts within the same process. The rendering contexts must be from the same OpenGL implementation. For example, you can always copy a rendering state between two rendering contexts with identical pixel format in the same process.

You can copy the same state information available only with the <b>glPushAttrib</b> function. You cannot copy some state information, such as pixel pack/unpack state, render mode state, select state, and feedback state. When you call <b>wglCopyContext</b>, make sure that the destination rendering context, <i>hglrcDst</i>, is not current to any thread.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/OpenGL/glpushattrib">glPushAttrib</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext">wglCreateLayerContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglsharelists">wglShareLists</a>