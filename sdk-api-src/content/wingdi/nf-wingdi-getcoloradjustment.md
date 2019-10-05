---
UID: NF:wingdi.GetColorAdjustment
title: GetColorAdjustment function (wingdi.h)
author: windows-sdk-content
description: The GetColorAdjustment function retrieves the color adjustment values for the specified device context (DC).
old-location: gdi\getcoloradjustment.htm
tech.root: gdi
ms.assetid: 405c0d0d-9433-4f4a-9957-5c42a0fb3a07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColorAdjustment, GetColorAdjustment function [Windows GDI], _win32_GetColorAdjustment, gdi.getcoloradjustment, wingdi/GetColorAdjustment
ms.topic: function
f1_keywords: 
 - "wingdi/GetColorAdjustment"
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetColorAdjustment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetColorAdjustment function


## -description


The <b>GetColorAdjustment</b> function retrieves the color adjustment values for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpca [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-coloradjustment">COLORADJUSTMENT</a> structure that receives the color adjustment values.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-coloradjustment">COLORADJUSTMENT</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colors">Colors Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setcoloradjustment">SetColorAdjustment</a>
 

 

