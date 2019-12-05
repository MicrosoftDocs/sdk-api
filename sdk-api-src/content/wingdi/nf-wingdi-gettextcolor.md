---
UID: NF:wingdi.GetTextColor
title: GetTextColor function (wingdi.h)
description: The GetTextColor function retrieves the current text color for the specified device context.
old-location: gdi\gettextcolor.htm
tech.root: gdi
ms.assetid: d3d91b86-5143-431a-ba18-b951b832d7b6
ms.date: 12/05/2018
ms.keywords: GetTextColor, GetTextColor function [Windows GDI], _win32_GetTextColor, gdi.gettextcolor, wingdi/GetTextColor
ms.topic: function
f1_keywords:
- wingdi/GetTextColor
dev_langs:
- c++
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
- ext-ms-win-gdi-font-l1-1-2.dll
- Ext-MS-Win-GDI-Font-L1-1-3.dll
- GDI32Full.dll
api_name:
- GetTextColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTextColor function


## -description


The <b>GetTextColor</b> function retrieves the current text color for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value is the current text color as a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID. No extended error information is available.




## -remarks



The text color defines the foreground color of characters drawn by using the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-settextcolor">SetTextColor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut</a>
 

 

