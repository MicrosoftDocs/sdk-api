---
UID: NF:wingdi.GetColorAdjustment
title: GetColorAdjustment function
author: windows-sdk-content
description: The GetColorAdjustment function retrieves the color adjustment values for the specified device context (DC).
old-location: gdi\getcoloradjustment.htm
old-project: gdi
ms.assetid: 405c0d0d-9433-4f4a-9957-5c42a0fb3a07
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetColorAdjustment, GetColorAdjustment function [Windows GDI], _win32_GetColorAdjustment, gdi.getcoloradjustment, wingdi/GetColorAdjustment
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
 - GetColorAdjustment
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetColorAdjustment function


## -description


The <b>GetColorAdjustment</b> function retrieves the color adjustment values for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpca [out]

A pointer to a <a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a> structure that receives the color adjustment values.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a>



<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/292d6cdc-cafa-438a-9392-a9c22e7d44a5">SetColorAdjustment</a>
 

 

