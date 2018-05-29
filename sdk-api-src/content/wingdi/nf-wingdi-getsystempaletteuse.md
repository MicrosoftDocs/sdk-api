---
UID: NF:wingdi.GetSystemPaletteUse
title: GetSystemPaletteUse function
author: windows-sdk-content
description: The GetSystemPaletteUse function retrieves the current state of the system (physical) palette for the specified device context (DC).
old-location: gdi\getsystempaletteuse.htm
old-project: gdi
ms.assetid: 0a9e7906-2f81-4fda-b03d-86feb0755327
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetSystemPaletteUse, GetSystemPaletteUse function [Windows GDI], _win32_GetSystemPaletteUse, gdi.getsystempaletteuse, wingdi/GetSystemPaletteUse
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
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetSystemPaletteUse
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetSystemPaletteUse function


## -description


The <b>GetSystemPaletteUse</b> function retrieves the current state of the system (physical) palette for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is the current state of the system palette. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SYSPAL_NOSTATIC</td>
<td>The system palette contains no static colors except black and white.</td>
</tr>
<tr>
<td>SYSPAL_STATIC</td>
<td>The system palette contains static colors that will not change when an application realizes its logical palette.</td>
</tr>
<tr>
<td>SYSPAL_ERROR</td>
<td>The given device context is invalid or does not support a color palette.</td>
</tr>
</table>
 




## -remarks



By default, the system palette contains 20 static colors that are not changed when an application realizes its logical palette. An application can gain access to most of these colors by calling the <a href="https://msdn.microsoft.com/6ff245d3-1bcc-4778-a595-c1eb16531ad3">SetSystemPaletteUse</a> function.

The device context identified by the <i>hdc</i> parameter must represent a device that supports color palettes.

An application can determine whether a device supports color palettes by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/6ff245d3-1bcc-4778-a595-c1eb16531ad3">SetSystemPaletteUse</a>
 

 

