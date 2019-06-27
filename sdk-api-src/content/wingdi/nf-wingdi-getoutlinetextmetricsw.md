---
UID: NF:wingdi.GetOutlineTextMetricsW
title: GetOutlineTextMetricsW function (wingdi.h)
author: windows-sdk-content
description: The GetOutlineTextMetrics function retrieves text metrics for TrueType fonts.
old-location: gdi\getoutlinetextmetrics.htm
tech.root: gdi
ms.assetid: b8c7a557-ca35-41a4-9043-8496e5b01564
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOutlineTextMetrics, GetOutlineTextMetrics function [Windows GDI], GetOutlineTextMetricsA, GetOutlineTextMetricsW, _win32_GetOutlineTextMetrics, gdi.getoutlinetextmetrics, wingdi/GetOutlineTextMetrics, wingdi/GetOutlineTextMetricsA, wingdi/GetOutlineTextMetricsW
ms.topic: function
f1_keywords: 
 - "wingdi/GetOutlineTextMetrics"
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetOutlineTextMetricsW (Unicode) and GetOutlineTextMetricsA (ANSI)
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
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetOutlineTextMetrics
 - GetOutlineTextMetricsA
 - GetOutlineTextMetricsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetOutlineTextMetricsW function


## -description


The <b>GetOutlineTextMetrics</b> function retrieves text metrics for TrueType fonts.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param cjCopy [in]

The size, in bytes, of the array that receives the text metrics.


### -param potm [out, optional]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-_outlinetextmetrica">OUTLINETEXTMETRIC</a> structure. If this parameter is <b>NULL</b>, the function returns the size of the buffer required for the retrieved metric data.


## -returns



If the function succeeds, the return value is nonzero or the size of the required buffer.

If the function fails, the return value is zero.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-_outlinetextmetrica">OUTLINETEXTMETRIC</a> structure contains most of the text metric information provided for TrueType fonts (including a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagtextmetrica">TEXTMETRIC</a> structure). The sizes returned in <b>OUTLINETEXTMETRIC</b> are in logical units; they depend on the current mapping mode.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-_outlinetextmetrica">OUTLINETEXTMETRIC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagtextmetrica">TEXTMETRIC</a>
 

 

