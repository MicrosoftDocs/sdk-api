---
UID: NF:wingdi.CreateSolidBrush
title: CreateSolidBrush function
author: windows-sdk-content
description: The CreateSolidBrush function creates a logical brush that has the specified solid color.
old-location: gdi\createsolidbrush.htm
tech.root: gdi
ms.assetid: e39b5f77-97d8-4ea6-8277-7da12b3367f3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateSolidBrush, CreateSolidBrush function [Windows GDI], _win32_CreateSolidBrush, gdi.createsolidbrush, wingdi/CreateSolidBrush
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateSolidBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateSolidBrush function


## -description


The <b>CreateSolidBrush</b> function creates a logical brush that has the specified solid color.


## -parameters




### -param color [in]

The color of the brush. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the <b>HBRUSH</b> object, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

A solid brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateSolidBrush</b>, it can select that brush into any device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function.

To paint with a system color brush, an application should use <code>GetSysColorBrush (nIndex)</code> instead of <code>CreateSolidBrush(GetSysColor(nIndex))</code>, because <a href="https://msdn.microsoft.com/07a1d8e3-eae8-40ab-9d0f-4efa9fac0117">GetSysColorBrush</a> returns a cached brush instead of allocating a new one.

<b>ICM:</b> No color management is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/2ea32786-f769-4096-8f60-f924c83ca9c8">Creating Colored Pens and Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a>



<a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/07a1d8e3-eae8-40ab-9d0f-4efa9fac0117">GetSysColorBrush</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

