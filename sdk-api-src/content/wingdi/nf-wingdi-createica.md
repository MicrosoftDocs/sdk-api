---
UID: NF:wingdi.CreateICA
title: CreateICA function
author: windows-driver-content
description: The CreateIC function creates an information context for the specified device.
old-location: gdi\createic.htm
old-project: gdi
ms.assetid: dcb08ce7-9ded-497c-936c-48d3026a0004
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CreateIC, CreateIC function [Windows GDI], CreateICA, CreateICW, _win32_CreateIC, gdi.createic, wingdi/CreateIC, wingdi/CreateICA, wingdi/CreateICW
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
req.unicode-ansi: CreateICW (Unicode) and CreateICA (ANSI)
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
-	Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
-	ext-ms-win-gdi-dc-create-l1-1-2.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	CreateIC
-	CreateICA
-	CreateICW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateICA function


## -description


The <b>CreateIC</b> function creates an information context for the specified device. The information context provides a fast way to get information about the device without creating a device context (DC). However, GDI drawing functions cannot accept a handle to an information context.


## -parameters




### -param pszDriver

TBD


### -param pszDevice

TBD


### -param pszPort

TBD


### -param pdm

TBD




#### - lpdvmInit [in]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure containing device-specific initialization data for the device driver. The <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a> function retrieves this structure filled in for a specified device. The <i>lpdvmInit</i> parameter must be <b>NULL</b> if the device driver is to use the default initialization (if any) specified by the user.


#### - lpszDevice [in]

A pointer to a null-terminated character string that specifies the name of the specific output device being used, as shown by the Print Manager (for example, Epson FX-80). It is not the printer model name. The <i>lpszDevice</i> parameter must be used.


#### - lpszDriver [in]

A pointer to a null-terminated character string that specifies the name of the device driver (for example, Epson).


#### - lpszOutput

This parameter is ignored and should be set to <b>NULL</b>. It is provided only for compatibility with 16-bit Windows.


## -returns



If the function succeeds, the return value is the handle to an information context.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the information DC, call the <a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>
 

 

