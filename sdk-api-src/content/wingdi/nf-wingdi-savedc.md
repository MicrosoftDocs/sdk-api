---
UID: NF:wingdi.SaveDC
title: SaveDC function
author: windows-sdk-content
description: The SaveDC function saves the current state of the specified device context (DC) by copying data describing selected objects and graphic modes (such as the bitmap, brush, palette, font, pen, region, drawing mode, and mapping mode) to a context stack.
old-location: gdi\savedc.htm
tech.root: gdi
ms.assetid: f438cd7f-436f-436c-b32e-67f5558740cb
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: SaveDC, SaveDC function [Windows GDI], _win32_SaveDC, gdi.savedc, wingdi/SaveDC
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
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - SaveDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SaveDC function


## -description


The <b>SaveDC</b> function saves the current state of the specified device context (DC) by copying data describing selected objects and graphic modes (such as the bitmap, brush, palette, font, pen, region, drawing mode, and mapping mode) to a context stack.


## -parameters




### -param hdc [in]

A handle to the DC whose state is to be saved.


## -returns



If the function succeeds, the return value identifies the saved state.

If the function fails, the return value is zero.




## -remarks



The <b>SaveDC</b> function can be used any number of times to save any number of instances of the DC state.

A saved state can be restored by using the <a href="https://msdn.microsoft.com/7043edbb-b3ea-4946-a2ba-cae356b04d1d">RestoreDC</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/7043edbb-b3ea-4946-a2ba-cae356b04d1d">RestoreDC
      </a>
 

 

