---
UID: NF:wingdi.GetColorSpace
title: GetColorSpace function (wingdi.h)
description: The GetColorSpace function retrieves the handle to the input color space from a specified device context.
helpviewer_keywords: ["GetColorSpace","GetColorSpace function [Windows Color System]","_color_GetColorSpace","wcs.getcolorspace","wingdi/GetColorSpace"]
old-location: wcs\getcolorspace.htm
tech.root: WCS
ms.assetid: 6d092755-2c7a-46a7-9127-df72c26c3ae9
ms.date: 12/05/2018
ms.keywords: GetColorSpace, GetColorSpace function [Windows Color System], _color_GetColorSpace, wcs.getcolorspace, wingdi/GetColorSpace
f1_keywords:
- wingdi/GetColorSpace
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetColorSpace function


## -description


The <b>GetColorSpace</b> function retrieves the handle to the input <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/c">color space</a> from a specified device context.


## -parameters




### -param hdc

Specifies a device context that is to have its input color space handle retrieved.


## -returns



If the function succeeds, the return value is the current input color space handle.

If this function fails, the return value is <b>NULL</b>.




## -remarks



<b>GetColorSpace</b> obtains the handle to the input color space regardless of whether color management is enabled for the device context.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>
 

 

