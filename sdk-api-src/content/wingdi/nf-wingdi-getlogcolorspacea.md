---
UID: NF:wingdi.GetLogColorSpaceA
title: GetLogColorSpaceA function (wingdi.h)
author: windows-sdk-content
description: The GetLogColorSpace function retrieves the color space definition identified by a specified handle.
old-location: wcs\getlogcolorspace.htm
tech.root: WCS
ms.assetid: 01862a48-8c2f-4b29-b928-2800c02218a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLogColorSpace, GetLogColorSpace function [Windows Color System], GetLogColorSpaceA, GetLogColorSpaceW, _color_GetLogColorSpace, wcs.getlogcolorspace, wingdi/GetLogColorSpace, wingdi/GetLogColorSpaceA, wingdi/GetLogColorSpaceW
ms.topic: function
f1_keywords: 
 - "wingdi/GetLogColorSpace"
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLogColorSpaceW (Unicode) and GetLogColorSpaceA (ANSI)
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
 - GetLogColorSpace
 - GetLogColorSpaceA
 - GetLogColorSpaceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetLogColorSpaceA function


## -description


The <b>GetLogColorSpace</b> function retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/c">color space</a> definition identified by a specified handle.


## -parameters




### -param hColorSpace

Specifies the handle to a color space.


### -param lpBuffer

Points to a buffer to receive the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a> structure.


### -param nSize

Specifies the maximum size of the buffer.


## -returns



If this function succeeds, the return value is TRUE.

If this function fails, the return value is <b>FALSE</b>.




## -remarks



<b>Windows 95/98/Me: </b><b>GetLogColorSpaceW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>
 

 

