---
UID: NF:wingdi.CreateCompatibleDC
title: CreateCompatibleDC function
author: windows-driver-content
description: The CreateCompatibleDC function creates a memory device context (DC) compatible with the specified device.
old-location: gdi\createcompatibledc.htm
old-project: gdi
ms.assetid: 6ddc3705-2995-41af-af94-258aed597e17
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CreateCompatibleDC, CreateCompatibleDC function [Windows GDI], _win32_CreateCompatibleDC, gdi.createcompatibledc, wingdi/CreateCompatibleDC
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
-	Ext-MS-Win-GDI-DC-Create-l1-1-0.dll
-	Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
-	ext-ms-win-gdi-dc-create-l1-1-2.dll
-	GDI32Full.dll
api_name:
-	CreateCompatibleDC
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateCompatibleDC function


## -description


The <b>CreateCompatibleDC</b> function creates a memory device context (DC) compatible with the specified device.


## -parameters




### -param hdc [in]

A handle to an existing DC. If this handle is <b>NULL</b>, the function creates a memory DC compatible with the application's current screen.


## -returns



If the function succeeds, the return value is the handle to a memory DC.

If the function fails, the return value is <b>NULL</b>.




## -remarks



A memory DC exists only in memory. When the memory DC is created, its display surface is exactly one monochrome pixel wide and one monochrome pixel high. Before an application can use a memory DC for drawing operations, it must select a bitmap of the correct width and height into the DC. To select a bitmap into a DC, use the <a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a> function, specifying the height, width, and color organization required.

When a memory DC is created, all attributes are set to normal default values. The memory DC can be used as a normal DC. You can set the attributes; obtain the current settings of its attributes; and select pens, brushes, and regions.

The <b>CreateCompatibleDC</b> function can only be used with devices that support raster operations. An application can determine whether a device supports these operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function.

When you no longer need the memory DC, call the <a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a> function. We recommend that you call <b>DeleteDC</b> to delete the DC.  However, you can also call <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">
                DeleteObject</a> with the HDC to delete the DC.


         If <i>hdc</i> is <b>NULL</b>, the thread that calls <b>CreateCompatibleDC</b> owns the HDC that is created. When this thread is destroyed, the HDC is no longer valid. Thus, if you create the HDC and pass it to another thread, then exit the first thread, the second thread will not be able to use the HDC.

<b>ICM:</b> If the DC that is passed to this function is enabled for Image Color Management (ICM), the DC created by the function is ICM-enabled. The source and destination color spaces are specified in the DC.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/672fc2e4-c35c-4d5d-98fa-85f2ad56d9b0">Capturing an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">
        CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">
        DeleteDC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">
        GetDeviceCaps</a>
 

 

