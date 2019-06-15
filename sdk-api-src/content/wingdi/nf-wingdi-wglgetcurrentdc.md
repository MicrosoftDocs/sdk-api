---
UID: NF:wingdi.wglGetCurrentDC
title: wglGetCurrentDC function (wingdi.h)
author: windows-sdk-content
description: The wglGetCurrentDC function obtains a handle to the device context that is associated with the current OpenGL rendering context of the calling thread.
old-location: opengl\wglgetcurrentdc.htm
tech.root: OpenGL
ms.assetid: 026f6181-75a2-4781-8762-d5599ce90af2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ogl_wglGetCurrentDC, opengl.wglgetcurrentdc, wglGetCurrentDC, wglGetCurrentDC function [OpenGL], wingdi/wglGetCurrentDC"
ms.topic: function
f1_keywords: ["wingdi/wglGetCurrentDC"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglGetCurrentDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# wglGetCurrentDC function


## -description


The <b>wglGetCurrentDC</b> function obtains a handle to the device context that is associated with the current OpenGL rendering context of the calling thread.


## -parameters






## -returns



If the calling thread has a current OpenGL rendering context, the function returns a handle to the device context associated with that rendering context by means of the <b>wglMakeCurrent</b> function. Otherwise, the return value is <b>NULL</b>.




## -remarks



You associate a device context with an OpenGL rendering context when it calls the <b>wglMakeCurrent</b> function. You can use the <b>wglGetCurrentContext</b> function to obtain a handle to the calling thread's current OpenGL rendering context.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="https://docs.microsoft.com/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext">wglCreateContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext">wglDeleteContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext">wglGetCurrentContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent">wglMakeCurrent</a>
 

 

