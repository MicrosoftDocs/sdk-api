---
UID: NF:wingdi.GetDCPenColor
title: GetDCPenColor function
author: windows-sdk-content
description: The GetDCPenColor function retrieves the current pen color for the specified device context (DC).
old-location: gdi\getdcpencolor.htm
old-project: gdi
ms.assetid: 3a1d579f-fbc6-4021-a37e-0184b2cc7d5d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDCPenColor, GetDCPenColor function [Windows GDI], _win32_GetDCPenColor, gdi.getdcpencolor, wingdi/GetDCPenColor
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
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetDCPenColor
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDCPenColor function


## -description


The <b>GetDCPenColor</b> function retrieves the current pen color for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC whose brush color is to be returned.


## -returns



If the function succeeds, the return value is a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value for the current DC pen color.

If the function fails, the return value is CLR_INVALID.




## -remarks



For information on setting the pen color, see <a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCPenColor</a>.

<b>ICM:</b> Color management is performed if ICM is enabled.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/057608eb-7209-4714-bf02-660a13d59016">SetDCPenColor</a>
 

 

