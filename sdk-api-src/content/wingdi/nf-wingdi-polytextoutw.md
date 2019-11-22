---
UID: NF:wingdi.PolyTextOutW
title: PolyTextOutW function (wingdi.h)

description: The PolyTextOut function draws several strings using the font and text colors currently selected in the specified device context.
old-location: gdi\polytextout.htm
tech.root: gdi
ms.assetid: 643b4f6a-843f-4795-adc8-a90223bdc246

ms.date: 12/05/2018
ms.keywords: PolyTextOut, PolyTextOut function [Windows GDI], PolyTextOutA, PolyTextOutW, _win32_PolyTextOut, gdi.polytextout, wingdi/PolyTextOut, wingdi/PolyTextOutA, wingdi/PolyTextOutW
ms.topic: function
f1_keywords: 
 - "wingdi/PolyTextOut"
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
req.unicode-ansi: PolyTextOutW (Unicode) and PolyTextOutA (ANSI)
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
 - PolyTextOut
 - PolyTextOutA
 - PolyTextOutW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PolyTextOutW function


## -description


The <b>PolyTextOut</b> function draws several strings using the font and text colors currently selected in the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param ppt [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-polytexta">POLYTEXT</a> structures describing the strings to be drawn. The array contains one structure for each string to be drawn.


### -param nstrings [in]

The number of <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-polytexta">POLYTEXT</a> structures in the <i>pptxt</i> array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Each <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-polytexta">POLYTEXT</a> structure contains the coordinates of a reference point that Windows uses to align the corresponding string of text. An application can specify how the reference point is used by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function. An application can determine the current text-alignment setting for the specified device context by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a> function.

To draw a single string of text, the application should call the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-polytexta">POLYTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a>
 

 

