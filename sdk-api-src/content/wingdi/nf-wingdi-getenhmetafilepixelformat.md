---
UID: NF:wingdi.GetEnhMetaFilePixelFormat
title: GetEnhMetaFilePixelFormat function (wingdi.h)
description: The GetEnhMetaFilePixelFormat function retrieves pixel format information for an enhanced metafile.
helpviewer_keywords: ["GetEnhMetaFilePixelFormat","GetEnhMetaFilePixelFormat function [OpenGL]","_ogl_GetEnhMetaFilePixelFormat","opengl.getenhmetafilepixelformat","wingdi/GetEnhMetaFilePixelFormat"]
old-location: opengl\getenhmetafilepixelformat.htm
tech.root: OpenGL
ms.assetid: 80209210-5caa-44a9-a791-991b257d8d28
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFilePixelFormat, GetEnhMetaFilePixelFormat function [OpenGL], _ogl_GetEnhMetaFilePixelFormat, opengl.getenhmetafilepixelformat, wingdi/GetEnhMetaFilePixelFormat
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
 - GetEnhMetaFilePixelFormat
 - wingdi/GetEnhMetaFilePixelFormat
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
 - GetEnhMetaFilePixelFormat
---

# GetEnhMetaFilePixelFormat function


## -description

The <b>GetEnhMetaFilePixelFormat</b> function retrieves pixel format information for an enhanced metafile.

## -parameters

### -param hemf

Identifies the enhanced metafile.

### -param cbBuffer

Specifies the size, in bytes, of the buffer into which the pixel format information is copied.

### -param ppfd

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure that contains the logical pixel format specification. The metafile uses this structure to record the logical pixel format specification.

## -returns

If the function succeeds and finds a pixel format, the return value is the size of the metafile's pixel format.

If no pixel format is present, the return value is zero.

If an error occurs and the function fails, the return value is GDI_ERROR. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When an enhanced metafile specifies a pixel format in its <b>ENHMETAHEADER</b> structure and the pixel format fits in the buffer, the pixel format information is copied into <i>ppfd</i>. When <i>cbBuffer</i> is too small to contain the pixel format of the metafile, the pixel format is not copied to the buffer. In either case, the function returns the size of the metafile's pixel format.

For information on metafile recording and other operations, see Enhanced Metafile Operations.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/win32-functions">Windows Functions</a>