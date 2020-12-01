---
UID: NF:wingdi.GetPixelFormat
title: GetPixelFormat function (wingdi.h)
description: The GetPixelFormat function obtains the index of the currently selected pixel format of the specified device context.
helpviewer_keywords: ["GetPixelFormat","GetPixelFormat function [OpenGL]","_ogl_GetPixelFormat","opengl.getpixelformat","wingdi/GetPixelFormat"]
old-location: opengl\getpixelformat.htm
tech.root: OpenGL
ms.assetid: e9a65f3a-6932-462f-b342-a993d222fae8
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat function [OpenGL], _ogl_GetPixelFormat, opengl.getpixelformat, wingdi/GetPixelFormat
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
 - GetPixelFormat
 - wingdi/GetPixelFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetPixelFormat
---

# GetPixelFormat function


## -description

The <b>GetPixelFormat</b> function obtains the index of the currently selected pixel format of the specified device context.

## -parameters

### -param hdc

Specifies the device context of the currently selected pixel format index returned by the function.

## -returns

If the function succeeds, the return value is the currently selected pixel format index of the specified device context. This is a positive, one-based index value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat">ChoosePixelFormat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-describepixelformat">DescribePixelFormat</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a>



<a href="/windows/desktop/OpenGL/win32-functions">Windows Functions</a>