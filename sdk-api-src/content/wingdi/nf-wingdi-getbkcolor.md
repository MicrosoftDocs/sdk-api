---
UID: NF:wingdi.GetBkColor
title: GetBkColor function (wingdi.h)
author: windows-sdk-content
description: The GetBkColor function returns the current background color for the specified device context.
old-location: gdi\getbkcolor.htm
tech.root: gdi
ms.assetid: 1c6e8d05-4b8d-476d-852c-f06f316cb8b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBkColor, GetBkColor function [Windows GDI], _win32_GetBkColor, gdi.getbkcolor, wingdi/GetBkColor
ms.topic: function
f1_keywords: 
 - "wingdi/GetBkColor"
req.header: wingdi.h
req.include-header: Windows.h
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
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetBkColor function


## -description


The <b>GetBkColor</b> function returns the current background color for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context whose background color is to be returned.


## -returns



If the function succeeds, the return value is a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value for the current background color.

If the function fails, the return value is CLR_INVALID.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getbkmode">GetBkMode</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>
 

 

