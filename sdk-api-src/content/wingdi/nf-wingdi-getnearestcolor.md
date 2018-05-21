---
UID: NF:wingdi.GetNearestColor
title: GetNearestColor function
author: windows-driver-content
description: The GetNearestColor function retrieves a color value identifying a color from the system palette that will be displayed when the specified color value is used.
old-location: gdi\getnearestcolor.htm
old-project: gdi
ms.assetid: 89e4e19b-47be-442e-8eb4-c867bb78f36a
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetNearestColor, GetNearestColor function [Windows GDI], _win32_GetNearestColor, gdi.getnearestcolor, wingdi/GetNearestColor
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetNearestColor
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetNearestColor function


## -description


The <b>GetNearestColor</b> function retrieves a color value identifying a color from the system palette that will be displayed when the specified color value is used.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param color

TBD




#### - crColor [in]

A color value that identifies a requested color. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value identifies a color from the system palette that corresponds to the given color value.

If the function fails, the return value is CLR_INVALID.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/df54532d-dcdb-4927-8f48-c9c92a7e0121">GetNearestPaletteIndex</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

