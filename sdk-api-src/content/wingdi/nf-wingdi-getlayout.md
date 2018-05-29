---
UID: NF:wingdi.GetLayout
title: GetLayout function
author: windows-sdk-content
description: The GetLayout function returns the layout of a device context (DC).
old-location: gdi\getlayout.htm
old-project: gdi
ms.assetid: 2bbc0bef-55e5-4f11-a195-d379e95e44bf
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetLayout, GetLayout function [Windows GDI], _win32_GetLayout, gdi.getlayout, wingdi/GetLayout
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	ext-ms-win-gdi-dc-l1-2-1.dll
-	GDI32Full.dll
api_name:
-	GetLayout
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetLayout function


## -description


The <b>GetLayout</b> function returns the layout of a device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, it returns the layout flags for the current device context.

If the function fails, it returns GDI_ERROR. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The layout specifies the order in which text and graphics are revealed in a window or device context. The default is left to right. The <b>GetLayout</b> function tells you if the default has been changed through a call to <a href="https://msdn.microsoft.com/81c6dccd-cfb1-486f-8c25-f46ba7c3ff8d">SetLayout</a>. For more information, see "Window Layout and Mirroring" in <a href="_win32_Window_Features_cpp">Window Features</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/81c6dccd-cfb1-486f-8c25-f46ba7c3ff8d">SetLayout</a>
 

 

