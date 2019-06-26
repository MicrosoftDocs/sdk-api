---
UID: NF:wingdi.CreateColorSpaceW
title: CreateColorSpaceW function (wingdi.h)
author: windows-sdk-content
description: The CreateColorSpace function creates a logical color space.
old-location: wcs\createcolorspace.htm
tech.root: WCS
ms.assetid: c3fc798c-4bb9-4010-87d4-edc0005b7698
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateColorSpace, CreateColorSpace function [Windows Color System], CreateColorSpaceA, CreateColorSpaceW, _color_CreateColorSpace, wcs.createcolorspace, wingdi/CreateColorSpace, wingdi/CreateColorSpaceA, wingdi/CreateColorSpaceW
ms.topic: function
f1_keywords: 
 - "wingdi/CreateColorSpace"
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateColorSpaceW (Unicode) and CreateColorSpaceA (ANSI)
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
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateColorSpace
 - CreateColorSpaceA
 - CreateColorSpaceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateColorSpaceW function


## -description


The <b>CreateColorSpace</b> function creates a logical <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/c">color space</a>.


## -parameters




### -param lplcs

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-taglogcolorspacea">LOGCOLORSPACE</a> data structure.


## -returns



If this function succeeds, the return value is a handle that identifies a color space.

If this function fails, the return value is <b>NULL</b>.




## -remarks



When the color space is no longer needed, use <b>DeleteColorSpace</b> to delete it.

<b>Windows 95/98/Me: </b><b>CreateColorSpaceW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deletecolorspace">DeleteColorSpace</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>
 

 

