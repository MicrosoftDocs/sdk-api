---
UID: NF:wingdi.SetColorAdjustment
title: SetColorAdjustment function
author: windows-sdk-content
description: The SetColorAdjustment function sets the color adjustment values for a device context (DC) using the specified values.
old-location: gdi\setcoloradjustment.htm
tech.root: gdi
ms.assetid: 292d6cdc-cafa-438a-9392-a9c22e7d44a5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SetColorAdjustment, SetColorAdjustment function [Windows GDI], _win32_SetColorAdjustment, gdi.setcoloradjustment, wingdi/SetColorAdjustment
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetColorAdjustment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetColorAdjustment function


## -description


The <b>SetColorAdjustment</b> function sets the color adjustment values for a device context (DC) using the specified values.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpca [in]

A pointer to a <a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a> structure containing the color adjustment values.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The color adjustment values are used to adjust the input color of the source bitmap for calls to the <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> and <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> functions when HALFTONE mode is set.




## -see-also




<a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a>



<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/405c0d0d-9433-4f4a-9957-5c42a0fb3a07">GetColorAdjustment</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

