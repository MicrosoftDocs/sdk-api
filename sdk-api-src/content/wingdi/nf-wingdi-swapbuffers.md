---
UID: NF:wingdi.SwapBuffers
title: SwapBuffers function (wingdi.h)
description: The SwapBuffers function exchanges the front and back buffers if the current pixel format for the window referenced by the specified device context includes a back buffer.
helpviewer_keywords: ["SwapBuffers","SwapBuffers function [OpenGL]","_ogl_SwapBuffers","opengl.swapbuffers","wingdi/SwapBuffers"]
old-location: opengl\swapbuffers.htm
tech.root: OpenGL
ms.assetid: 2c9728e4-c5be-4b14-a6f7-2899c792ec3d
ms.date: 12/05/2018
ms.keywords: SwapBuffers, SwapBuffers function [OpenGL], _ogl_SwapBuffers, opengl.swapbuffers, wingdi/SwapBuffers
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
 - SwapBuffers
 - wingdi/SwapBuffers
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
 - SwapBuffers
---

# SwapBuffers function


## -description

The <b>SwapBuffers</b> function exchanges the front and back buffers if the current pixel format for the window referenced by the specified device context includes a back buffer.

## -parameters

### -param unnamedParam1

Specifies a device context. If the current pixel format for the window referenced by this device context includes a back buffer, the function exchanges the front and back buffers.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the current pixel format for the window referenced by the device context does not include a back buffer, this call has no effect and the content of the back buffer is undefined when the function returns.

With multithread applications, flush the drawing commands in any other threads drawing to the same window before calling <b>SwapBuffers</b>.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/win32-functions">Windows Functions</a>