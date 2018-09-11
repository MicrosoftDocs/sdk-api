---
UID: NF:wingdi.wglGetCurrentDC
title: wglGetCurrentDC function
author: windows-sdk-content
description: The wglGetCurrentDC function obtains a handle to the device context that is associated with the current OpenGL rendering context of the calling thread.
old-location: opengl\wglgetcurrentdc.htm
tech.root: OpenGL
ms.assetid: 026f6181-75a2-4781-8762-d5599ce90af2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ogl_wglGetCurrentDC, opengl.wglgetcurrentdc, wglGetCurrentDC, wglGetCurrentDC function [OpenGL], wingdi/wglGetCurrentDC"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a>



<a href="https://msdn.microsoft.com/51d4cce1-fd2d-436e-816b-b89d3cd66f3a">wglDeleteContext</a>



<a href="https://msdn.microsoft.com/8e2a4f24-689c-48b7-a06e-fc57d65b5567">wglGetCurrentContext</a>



<a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>
 

 

