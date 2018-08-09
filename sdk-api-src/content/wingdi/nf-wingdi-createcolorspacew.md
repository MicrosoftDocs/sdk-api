---
UID: NF:wingdi.CreateColorSpaceW
title: CreateColorSpaceW function
author: windows-sdk-content
description: The CreateColorSpace function creates a logical color space.
old-location: wcs\createcolorspace.htm
old-project: WCS
ms.assetid: c3fc798c-4bb9-4010-87d4-edc0005b7698
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CreateColorSpace, CreateColorSpace function [Windows Color System], CreateColorSpaceA, CreateColorSpaceW, _color_CreateColorSpace, wcs.createcolorspace, wingdi/CreateColorSpace, wingdi/CreateColorSpaceA, wingdi/CreateColorSpaceW
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
req.unicode-ansi: CreateColorSpaceW (Unicode) and CreateColorSpaceA (ANSI)
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
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateColorSpace
 - CreateColorSpaceA
 - CreateColorSpaceW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateColorSpaceW function


## -description


The <b>CreateColorSpace</b> function creates a logical <a href="https://msdn.microsoft.com/en-us/library/Dd371818(v=VS.85).aspx">color space</a>.


## -parameters




### -param lplcs

Pointer to the <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a> data structure.


## -returns



If this function succeeds, the return value is a handle that identifies a color space.

If this function fails, the return value is <b>NULL</b>.




## -remarks



When the color space is no longer needed, use <b>DeleteColorSpace</b> to delete it.

<b>Windows 95/98/Me: </b><b>CreateColorSpaceW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/5b241224-2994-4533-9629-d2a4b129ce86">DeleteColorSpace</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

