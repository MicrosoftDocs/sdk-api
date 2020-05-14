---
UID: NF:wingdi.GetTextMetricsW
title: GetTextMetricsW function (wingdi.h)
description: The GetTextMetrics function fills the specified buffer with the metrics for the currently selected font.helpviewer_keywords: ["GetTextMetrics","GetTextMetrics function [Windows GDI]","GetTextMetricsA","GetTextMetricsW","_win32_GetTextMetrics","gdi.gettextmetrics","wingdi/GetTextMetrics","wingdi/GetTextMetricsA","wingdi/GetTextMetricsW"]
old-location: gdi\gettextmetrics.htm
tech.root: gdi
ms.assetid: 92d45a3b-12df-42ff-8d87-5c27b44dc481
ms.date: 12/05/2018
ms.keywords: GetTextMetrics, GetTextMetrics function [Windows GDI], GetTextMetricsA, GetTextMetricsW, _win32_GetTextMetrics, gdi.gettextmetrics, wingdi/GetTextMetrics, wingdi/GetTextMetricsA, wingdi/GetTextMetricsW
f1_keywords:
- wingdi/GetTextMetrics
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
req.unicode-ansi: GetTextMetricsW (Unicode) and GetTextMetricsA (ANSI)
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
- Ext-MS-Win-GDI-Font-l1-1-0.dll
- Ext-MS-Win-GDI-Font-l1-1-1.dll
- ext-ms-win-gdi-font-l1-1-2.dll
- Ext-MS-Win-GDI-Font-L1-1-3.dll
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32Full.dll
api_name:
- GetTextMetrics
- GetTextMetricsA
- GetTextMetricsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTextMetricsW function


## -description


The <b>GetTextMetrics</b> function fills the specified buffer with the metrics for the currently selected font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lptm [out]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a> structure that receives the text metrics.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To determine whether a font is a TrueType font, first select it into a DC, then call <b>GetTextMetrics</b>, and then check for TMPF_TRUETYPE in TEXTMETRIC.tmPitchAndFamily. Note that <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> returns an uninitialized DC, which has "System" (a bitmap font) as the default font; thus the need to select a font into the DC.


#### Examples

For an example, see "Displaying Keyboard Input" in <a href="https://docs.microsoft.com/windows/desktop/inputdev/using-keyboard-input">Using Keyboard Input</a> or <a href="https://docs.microsoft.com/windows/desktop/gdi/drawing-text-from-different-fonts-on-the-same-line">Drawing Text from Different Fonts on the Same Line</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextfacea">GetTextFace</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-settextjustification">SetTextJustification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a>
 

 

