---
UID: NF:wingdi.GetPixelFormat
title: GetPixelFormat function
author: windows-sdk-content
description: The GetPixelFormat function obtains the index of the currently selected pixel format of the specified device context.
old-location: opengl\getpixelformat.htm
tech.root: OpenGL
ms.assetid: e9a65f3a-6932-462f-b342-a993d222fae8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetPixelFormat, GetPixelFormat function [OpenGL], _ogl_GetPixelFormat, opengl.getpixelformat, wingdi/GetPixelFormat
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPixelFormat function


## -description


The <b>GetPixelFormat</b> function obtains the index of the currently selected pixel format of the specified device context.


## -parameters




### -param hdc

Specifies the device context of the currently selected pixel format index returned by the function.


## -returns



If the function succeeds, the return value is the currently selected pixel format index of the specified device context. This is a positive, one-based index value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/17bd0a2c-5257-4ae3-80f4-a5ad536169fb">ChoosePixelFormat</a>



<a href="https://msdn.microsoft.com/9692a30d-c7d4-40c7-a265-72c4ebabd5f2">DescribePixelFormat</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/866841db-b137-4f65-856d-b9df5bde12fb">Windows Functions</a>
 

 

