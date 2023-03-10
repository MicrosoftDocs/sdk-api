---
UID: NF:wingdi.wglShareLists
title: wglShareLists function (wingdi.h)
description: The wglShareLists function enables multiple OpenGL rendering contexts to share a single display-list space.
helpviewer_keywords: ["_ogl_wglShareLists","opengl.wglsharelists","wglShareLists","wglShareLists function [OpenGL]","wingdi/wglShareLists"]
old-location: opengl\wglsharelists.htm
tech.root: OpenGL
ms.assetid: 587ea116-c70b-41ca-bf9b-a0c666f4e948
ms.date: 12/05/2018
ms.keywords: _ogl_wglShareLists, opengl.wglsharelists, wglShareLists, wglShareLists function [OpenGL], wingdi/wglShareLists
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
 - wglShareLists
 - wingdi/wglShareLists
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
 - wglShareLists
---

# wglShareLists function


## -description

The <b>wglShareLists</b> function enables multiple OpenGL rendering contexts to share a single display-list space.

## -parameters

### -param unnamedParam1

Specifies the OpenGL rendering context with which to share display lists.

### -param unnamedParam2

Specifies the OpenGL rendering context to share display lists with <i>hglrc1</i>. The <i>hglrc2</i> parameter should not contain any existing display lists when <b>wglShareLists</b> is called.

## -returns

When the function succeeds, the return value is <b>TRUE</b>.

When the function fails, the return value is <b>FALSE</b> and the display lists are not shared. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When you create an OpenGL rendering context, it has its own display-list space. The <b>wglShareLists</b> function enables a rendering context to share the display-list space of another rendering context; any number of rendering contexts can share a single display-list space. Once a rendering context shares a display-list space, the rendering context always uses the display-list space until the rendering context is deleted. When the last rendering context of a shared display-list space is deleted, the shared display-list space is deleted. All the indexes and definitions of display lists in a shared display-list space are shared.

You can only share display lists with rendering contexts within the same process. However, not all rendering contexts in a process can share display lists. Rendering contexts can share display lists only if they use the same implementation of OpenGL functions. All client rendering contexts of a given pixel format can always share display lists.

All rendering contexts of a shared display list must use an identical pixel format. Otherwise the results depend on the implementation of OpenGL used.

<div class="alert"><b>Note</b>  The <b>wglShareLists</b> function is only available with OpenGL version 1.01 or later. To determine the version number of the implementation of OpenGL, call <b>glGetString</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/OpenGL/glgetstring">glGetString</a>