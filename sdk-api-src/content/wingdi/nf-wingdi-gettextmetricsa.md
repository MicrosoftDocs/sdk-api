---
UID: NF:wingdi.GetTextMetricsA
title: GetTextMetricsA function
author: windows-sdk-content
description: The GetTextMetrics function fills the specified buffer with the metrics for the currently selected font.
old-location: gdi\gettextmetrics.htm
tech.root: gdi
ms.assetid: 92d45a3b-12df-42ff-8d87-5c27b44dc481
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetTextMetrics, GetTextMetrics function [Windows GDI], GetTextMetricsA, GetTextMetricsW, _win32_GetTextMetrics, gdi.gettextmetrics, wingdi/GetTextMetrics, wingdi/GetTextMetricsA, wingdi/GetTextMetricsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextMetricsA function


## -description


The <b>GetTextMetrics</b> function fills the specified buffer with the metrics for the currently selected font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lptm [out]

A pointer to the <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a> structure that receives the text metrics.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To determine whether a font is a TrueType font, first select it into a DC, then call <b>GetTextMetrics</b>, and then check for TMPF_TRUETYPE in TEXTMETRIC.tmPitchAndFamily. Note that <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> returns an uninitialized DC, which has "System" (a bitmap font) as the default font; thus the need to select a font into the DC.


#### Examples

For an example, see "Displaying Keyboard Input" in <a href="https://msdn.microsoft.com/en-us/library/ms646268(v=VS.85).aspx">Using Keyboard Input</a> or <a href="https://msdn.microsoft.com/d21613ef-1ba4-40bb-b922-afe287556441">Drawing Text from Different Fonts on the Same Line</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/c4c8c8f5-3651-481b-a55f-da7f49d92f3a">GetTextFace</a>



<a href="https://msdn.microsoft.com/55fb5a28-b7da-40d8-8e64-4b42c23fa8b1">SetTextJustification</a>



<a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a>
 

 

