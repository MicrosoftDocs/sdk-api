---
UID: NF:wingdi.CreateDCW
title: CreateDCW function
author: windows-driver-content
description: The CreateDC function creates a device context (DC) for a device using the specified name.
old-location: gdi\createdc.htm
old-project: gdi
ms.assetid: 6fc443c8-da97-4196-a9ed-179a4e583849
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: CreateDC, CreateDC function [Windows GDI], CreateDCA, CreateDCW, _win32_CreateDC, gdi.createdc, wingdi/CreateDC, wingdi/CreateDCA, wingdi/CreateDCW
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
req.unicode-ansi: CreateDCW (Unicode) and CreateDCA (ANSI)
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
-	CreateDC
-	CreateDCA
-	CreateDCW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateDCW function


## -description


The <b>CreateDC</b> function creates a device context (DC) for a device using the specified name.


## -parameters




### -param pwszDriver

TBD


### -param pwszDevice

TBD


### -param pszPort

TBD


### -param pdm

TBD




#### - lpInitData [in]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure containing device-specific initialization data for the device driver. The <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a> function retrieves this structure filled in for a specified device. The <i>lpInitData</i> parameter must be <b>NULL</b> if the device driver is to use the default initialization (if any) specified by the user.

If <i>lpszDriver</i> is DISPLAY, <i>lpInitData</i> must be <b>NULL</b>; GDI then uses the display device's current <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>.


#### - lpszDevice [in]

A pointer to a null-terminated character string that specifies the name of the specific output device being used, as shown by the Print Manager (for example, Epson FX-80). It is not the printer model name. The <i>lpszDevice</i> parameter must be used.

To obtain valid names for displays, call <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>.

If <i>lpszDriver</i> is DISPLAY or the device name of a specific display device, then <i>lpszDevice</i> must be <b>NULL</b> or that same device name. If <i>lpszDevice</i> is <b>NULL</b>, then a DC is created for the primary display device.

If there are multiple monitors on the system, calling <code>CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL)</code> will create a DC covering all the monitors.


#### - lpszDriver

A pointer to a null-terminated character string that specifies either DISPLAY or the name of a specific display device. For printing, we recommend that you pass <b>NULL</b> to <i>lpszDriver</i> because GDI ignores <i>lpszDriver</i> for printer devices.


#### - lpszOutput

This parameter is ignored and should be set to <b>NULL</b>. It is provided only for compatibility with 16-bit Windows.


## -returns



If the function succeeds, the return value is the handle to a DC for the specified device.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Note that the handle to the DC can only be used by a single thread at any one time.

For parameters <i>lpszDriver</i> and <i>lpszDevice</i>, call <a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a> to obtain valid names for displays.

When you no longer need the DC, call the <a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a> function.


         If <i>lpszDriver</i> or <i>lpszDevice</i> is DISPLAY, the thread that calls <b>CreateDC</b> owns the <b>HDC</b> that is created. When this thread is destroyed, the <b>HDC</b> is no longer valid. Thus, if you create the <b>HDC</b> and pass it to another thread, then exit the first thread, the second thread will not be able to use the <b>HDC</b>.

When you call <b>CreateDC</b> to create the <b>HDC</b> for a display device, you must pass to <i>lpInitData</i> either <b>NULL</b> or a pointer to <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> that matches the current <b>DEVMODE</b> of the display device that <i>lpszDevice</i> specifies. We recommend to pass <b>NULL</b> and not to try to exactly match the <b>DEVMODE</b> for the current display device.

When you call <b>CreateDC</b> to create the <b>HDC</b> for a printer device, the printer driver validates the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>. If the printer driver determines that the <b>DEVMODE</b> is invalid (that is, printer driver can’t convert or consume the DEVMODE), the printer driver provides a default <b>DEVMODE</b> to create the HDC for the printer device.

<b>ICM:</b> To enable ICM, set the <b>dmICMMethod</b> member of the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure (pointed to by the <i>pInitData</i> parameter) to the appropriate value.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/672fc2e4-c35c-4d5d-98fa-85f2ad56d9b0">Capturing an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/329bf0d9-399b-4f64-a029-361ef7558aeb">DOCINFO</a>



<a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>



<a href="https://msdn.microsoft.com/df3b493c-23d2-4996-9b79-86009efe3078">EnumDisplayDevices</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>
 

 

