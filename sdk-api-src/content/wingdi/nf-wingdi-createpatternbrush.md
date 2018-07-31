---
UID: NF:wingdi.CreatePatternBrush
title: CreatePatternBrush function
author: windows-sdk-content
description: The CreatePatternBrush function creates a logical brush with the specified bitmap pattern. The bitmap can be a DIB section bitmap, which is created by the CreateDIBSection function, or it can be a device-dependent bitmap.
old-location: gdi\createpatternbrush.htm
old-project: gdi
ms.assetid: a3cf347e-9803-4bb0-bdb3-98929ef859ab
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreatePatternBrush, CreatePatternBrush function [Windows GDI], _win32_CreatePatternBrush, gdi.createpatternbrush, wingdi/CreatePatternBrush
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
 - CreatePatternBrush
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreatePatternBrush function


## -description


The <b>CreatePatternBrush</b> function creates a logical brush with the specified bitmap pattern. The bitmap can be a DIB section bitmap, which is created by the <b>CreateDIBSection</b> function, or it can be a device-dependent bitmap.


## -parameters




### -param hbm

TBD




#### - hbmp [in]

A handle to the bitmap to be used to create the logical brush.


## -returns



If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.




## -remarks



A pattern brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreatePatternBrush</b>, it can select that brush into any device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function.

You can delete a pattern brush without affecting the associated bitmap by using the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function. Therefore, you can then use this bitmap to create any number of pattern brushes.

A brush created by using a monochrome (1 bit per pixel) bitmap has the text and background colors of the device context to which it is drawn. Pixels represented by a 0 bit are drawn with the current text color; pixels represented by a 1 bit are drawn with the current background color.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/64cd6e82-7a0d-4b5e-b491-450f37eea43a">Using Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>



<a href="https://msdn.microsoft.com/79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5">CreateBitmapIndirect</a>



<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/0b938237-cb06-4776-86f8-14478abcee00">GetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>
 

 

