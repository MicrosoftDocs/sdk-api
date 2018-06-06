---
UID: NF:wingdi.wglDeleteContext
title: wglDeleteContext function
author: windows-sdk-content
description: The wglDeleteContext function deletes a specified OpenGL rendering context.
old-location: opengl\wgldeletecontext.htm
old-project: OpenGL
ms.assetid: 51d4cce1-fd2d-436e-816b-b89d3cd66f3a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "_ogl_wglDeleteContext, opengl.wgldeletecontext, wglDeleteContext, wglDeleteContext function [OpenGL], wingdi/wglDeleteContext"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglDeleteContext
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wglDeleteContext function


## -description


The <b>wglDeleteContext</b> function deletes a specified OpenGL rendering context.


## -parameters




### -param Arg1

TBD




#### - hglrc

Handle to an OpenGL rendering context that the function will delete.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



It is an error to delete an OpenGL rendering context that is the current context of another thread. However, if a rendering context is the calling thread's current context, the <b>wglDeleteContext</b> function changes the rendering context to being not current before deleting it.

The <b>wglDeleteContext</b> function does not delete the device context associated with the OpenGL rendering context when you call the <b>wglMakeCurrent</b> function. After calling <b>wglDeleteContext</b>, you must call <a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a> to delete the associated device context.




## -see-also




<a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a>



<a href="https://msdn.microsoft.com/8e2a4f24-689c-48b7-a06e-fc57d65b5567">wglGetCurrentContext</a>



<a href="https://msdn.microsoft.com/026f6181-75a2-4781-8762-d5599ce90af2">wglGetCurrentDC</a>



<a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>
 

 

