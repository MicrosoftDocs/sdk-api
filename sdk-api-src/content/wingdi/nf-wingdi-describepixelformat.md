---
UID: NF:wingdi.DescribePixelFormat
title: DescribePixelFormat function (wingdi.h)
description: The DescribePixelFormat function obtains information about the pixel format identified by iPixelFormat of the device associated with hdc. The function sets the members of the PIXELFORMATDESCRIPTOR structure pointed to by ppfd with that pixel format data.
helpviewer_keywords: ["DescribePixelFormat","DescribePixelFormat function [OpenGL]","_ogl_DescribePixelFormat","opengl.describepixelformat","wingdi/DescribePixelFormat"]
old-location: opengl\describepixelformat.htm
tech.root: OpenGL
ms.assetid: 9692a30d-c7d4-40c7-a265-72c4ebabd5f2
ms.date: 12/05/2018
ms.keywords: DescribePixelFormat, DescribePixelFormat function [OpenGL], _ogl_DescribePixelFormat, opengl.describepixelformat, wingdi/DescribePixelFormat
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
 - DescribePixelFormat
 - wingdi/DescribePixelFormat
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
 - DescribePixelFormat
---

# DescribePixelFormat function


## -description

The <b>DescribePixelFormat</b> function obtains information about the pixel format identified by <i>iPixelFormat</i> of the device associated with <i>hdc</i>. The function sets the members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure pointed to by <i>ppfd</i> with that pixel format data.

## -parameters

### -param hdc

Specifies the device context.

### -param iPixelFormat

Index that specifies the pixel format. The pixel formats that a device context supports are identified by positive one-based integer indexes.

### -param nBytes

The size, in bytes, of the structure pointed to by <i>ppfd</i>. The <b>DescribePixelFormat</b> function stores no more than <i>nBytes</i> bytes of data to that structure. Set this value to <b>sizeof</b>(<b>PIXELFORMATDESCRIPTOR</b>).

### -param ppfd

Pointer to a <b>PIXELFORMATDESCRIPTOR</b> structure whose members the function sets with pixel format data. The function stores the number of bytes copied to the structure in the structure's <b>nSize</b> member. If, upon entry, <i>ppfd</i> is <b>NULL</b>, the function writes no data to the structure. This is useful when you only want to obtain the maximum pixel format index of a device context.

## -returns

If the function succeeds, the return value is the maximum pixel format index of the device context. In addition, the function sets the members of the <b>PIXELFORMATDESCRIPTOR</b> structure pointed to by <i>ppfd</i> according to the specified pixel format.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat">ChoosePixelFormat</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpixelformat">GetPixelFormat</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixelformat">SetPixelFormat</a>



<a href="/windows/desktop/OpenGL/win32-functions">Windows Functions</a>