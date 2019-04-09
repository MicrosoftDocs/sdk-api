---
UID: NF:wingdi.GetOutlineTextMetricsA
title: GetOutlineTextMetricsA function (wingdi.h)
author: windows-sdk-content
description: The GetOutlineTextMetrics function retrieves text metrics for TrueType fonts.
old-location: gdi\getoutlinetextmetrics.htm
tech.root: gdi
ms.assetid: b8c7a557-ca35-41a4-9043-8496e5b01564
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOutlineTextMetrics, GetOutlineTextMetrics function [Windows GDI], GetOutlineTextMetricsA, GetOutlineTextMetricsW, _win32_GetOutlineTextMetrics, gdi.getoutlinetextmetrics, wingdi/GetOutlineTextMetrics, wingdi/GetOutlineTextMetricsA, wingdi/GetOutlineTextMetricsW
ms.topic: function
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
---

# GetOutlineTextMetricsA function


## -description


The <b>GetOutlineTextMetrics</b> function retrieves text metrics for TrueType fonts.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param cjCopy [in]

The size, in bytes, of the array that receives the text metrics.


### -param potm [out, optional]

A pointer to an <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure. If this parameter is <b>NULL</b>, the function returns the size of the buffer required for the retrieved metric data.


## -returns



If the function succeeds, the return value is nonzero or the size of the required buffer.

If the function fails, the return value is zero.




## -remarks



The <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure contains most of the text metric information provided for TrueType fonts (including a <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a> structure). The sizes returned in <b>OUTLINETEXTMETRIC</b> are in logical units; they depend on the current mapping mode.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>



<a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a>



<a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a>
 

 

