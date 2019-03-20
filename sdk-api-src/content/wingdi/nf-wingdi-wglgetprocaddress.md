---
UID: NF:wingdi.wglGetProcAddress
title: wglGetProcAddress function (wingdi.h)
author: windows-sdk-content
description: The wglGetProcAddress function returns the address of an OpenGL extension function for use with the current OpenGL rendering context.
old-location: opengl\wglgetprocaddress.htm
tech.root: OpenGL
ms.assetid: 7c419b64-1bc6-492e-9853-98b08f38a5ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ogl_wglGetProcAddress, opengl.wglgetprocaddress, wglGetProcAddress, wglGetProcAddress function [OpenGL], wingdi/wglGetProcAddress"
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
 - wglGetProcAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# wglGetProcAddress function


## -description


The <b>wglGetProcAddress</b> function returns the address of an OpenGL extension function for use with the current OpenGL rendering context.


## -parameters




### -param Arg1

Points to a <b>null</b>-terminated string that is the name of the extension function. The name of the extension function must be identical to a corresponding function implemented by OpenGL.


## -returns



When the function succeeds, the return value is the address of the extension function.

When no current rendering context exists or the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The OpenGL library supports multiple implementations of its functions. Extension functions supported in one rendering context are not necessarily available in a separate rendering context. Thus, for a given rendering context in an application, use the function addresses returned by the <b>wglGetProcAddress</b> function only.

The spelling and the case of the extension function pointed to by <i>lpszProc</i> must be identical to that of a function supported and implemented by OpenGL. Because extension functions are not exported by OpenGL, you must use <b>wglGetProcAddress</b> to get the addresses of vendor-specific extension functions.

The extension function addresses are unique for each pixel format. All rendering contexts of a given pixel format share the same extension function addresses.




## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>
 

 

