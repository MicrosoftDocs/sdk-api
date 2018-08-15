---
UID: NF:wingdi.DescribePixelFormat
title: DescribePixelFormat function
author: windows-sdk-content
description: The DescribePixelFormat function obtains information about the pixel format identified by iPixelFormat of the device associated with hdc. The function sets the members of the PIXELFORMATDESCRIPTOR structure pointed to by ppfd with that pixel format data.
old-location: opengl\describepixelformat.htm
old-project: OpenGL
ms.assetid: 9692a30d-c7d4-40c7-a265-72c4ebabd5f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DescribePixelFormat, DescribePixelFormat function [OpenGL], _ogl_DescribePixelFormat, opengl.describepixelformat, wingdi/DescribePixelFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: 
req.redist: 
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
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - DescribePixelFormat
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DescribePixelFormat function


## -description


The <b>DescribePixelFormat</b> function obtains information about the pixel format identified by <i>iPixelFormat</i> of the device associated with <i>hdc</i>. The function sets the members of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure pointed to by <i>ppfd</i> with that pixel format data.


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

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/17bd0a2c-5257-4ae3-80f4-a5ad536169fb">ChoosePixelFormat</a>



<a href="https://msdn.microsoft.com/e9a65f3a-6932-462f-b342-a993d222fae8">GetPixelFormat</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/866841db-b137-4f65-856d-b9df5bde12fb">Windows Functions</a>
 

 

