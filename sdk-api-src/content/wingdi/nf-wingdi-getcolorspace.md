---
UID: NF:wingdi.GetColorSpace
title: GetColorSpace function
author: windows-sdk-content
description: The GetColorSpace function retrieves the handle to the input color space from a specified device context.
old-location: wcs\getcolorspace.htm
tech.root: WCS
ms.assetid: 6d092755-2c7a-46a7-9127-df72c26c3ae9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetColorSpace, GetColorSpace function [Windows Color System], _color_GetColorSpace, wcs.getcolorspace, wingdi/GetColorSpace
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
 - GetColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetColorSpace function


## -description


The <b>GetColorSpace</b> function retrieves the handle to the input <a href="https://msdn.microsoft.com/en-us/library/Dd371818(v=VS.85).aspx">color space</a> from a specified device context.


## -parameters




### -param hdc

Specifies a device context that is to have its input color space handle retrieved.


## -returns



If the function succeeds, the return value is the current input color space handle.

If this function fails, the return value is <b>NULL</b>.




## -remarks



<b>GetColorSpace</b> obtains the handle to the input color space regardless of whether color management is enabled for the device context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

