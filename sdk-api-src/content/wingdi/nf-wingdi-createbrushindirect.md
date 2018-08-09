---
UID: NF:wingdi.CreateBrushIndirect
title: CreateBrushIndirect function
author: windows-sdk-content
description: The CreateBrushIndirect function creates a logical brush that has the specified style, color, and pattern.
old-location: gdi\createbrushindirect.htm
old-project: gdi
ms.assetid: 75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateBrushIndirect, CreateBrushIndirect function [Windows GDI], _win32_CreateBrushIndirect, gdi.createbrushindirect, wingdi/CreateBrushIndirect
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateBrushIndirect
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateBrushIndirect function


## -description


The <b>CreateBrushIndirect</b> function creates a logical brush that has the specified style, color, and pattern.


## -parameters




### -param plbrush [in]

A pointer to a <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a> structure that contains information about the brush.


## -returns



If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.




## -remarks



A brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateBrushIndirect</b>, it can select it into any device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function.

A brush created by using a monochrome bitmap (one color plane, one bit per pixel) is drawn using the current text and background colors. Pixels represented by a bit set to 0 are drawn with the current text color; pixels represented by a bit set to 1 are drawn with the current background color.

When you no longer need the brush, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

<b>ICM:</b> No color is done at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.




## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/0b938237-cb06-4776-86f8-14478abcee00">GetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>
 

 

