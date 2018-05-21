---
UID: NF:wingdi.GetDCBrushColor
title: GetDCBrushColor function
author: windows-driver-content
description: The GetDCBrushColor function retrieves the current brush color for the specified device context (DC).
old-location: gdi\getdcbrushcolor.htm
old-project: gdi
ms.assetid: 98844fb1-7ad8-4fbd-be59-9a19065253da
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetDCBrushColor, GetDCBrushColor function [Windows GDI], _win32_GetDCBrushColor, gdi.getdcbrushcolor, wingdi/GetDCBrushColor
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
-	Gdi32.dll
-	ext-ms-win-gdi-dc-l1-2-1.dll
-	GDI32Full.dll
api_name:
-	GetDCBrushColor
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDCBrushColor function


## -description


The <b>GetDCBrushColor</b> function retrieves the current brush color for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC whose brush color is to be returned.


## -returns



If the function succeeds, the return value is the <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value for the current DC brush color.

If the function fails, the return value is CLR_INVALID.




## -remarks



For information on setting the brush color, see <a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a>.

<b>ICM:</b> Color management is performed if ICM is enabled.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a>
 

 

