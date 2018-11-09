---
UID: NF:wingdi.ResetDCA
title: ResetDCA function
author: windows-sdk-content
description: The ResetDC function updates the specified printer or plotter device context (DC) using the specified information.
old-location: gdi\resetdc.htm
tech.root: gdi
ms.assetid: 3f77db51-90d1-4a87-812b-1e129ae8fde9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ResetDC, ResetDC function [Windows GDI], ResetDCA, ResetDCW, _win32_ResetDC, gdi.resetdc, wingdi/ResetDC, wingdi/ResetDCA, wingdi/ResetDCW
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
req.unicode-ansi: ResetDCW (Unicode) and ResetDCA (ANSI)
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
 - ResetDC
 - ResetDCA
 - ResetDCW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResetDCA function


## -description


The <b>ResetDC</b> function updates the specified printer or plotter device context (DC) using the specified information.


## -parameters




### -param hdc [in]

A handle to the DC to update.


### -param lpdm [in]

A pointer to a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure containing information about the new DC.


## -returns



If the function succeeds, the return value is a handle to the original DC.

If the function fails, the return value is <b>NULL</b>.




## -remarks



An application will typically use the <b>ResetDC</b> function when a window receives a <a href="https://msdn.microsoft.com/06b625a8-7584-4a98-b8e7-f1de668c274e">WM_DEVMODECHANGE</a> message. <b>ResetDC</b> can also be used to change the paper orientation or paper bins while printing a document.

The <b>ResetDC</b> function cannot be used to change the driver name, device name, or the output port. When the user changes the port connection or device name, the application must delete the original DC and create a new DC with the new information.

An application can pass an information DC to the <b>ResetDC</b> function. In that situation, <b>ResetDC</b> will always return a printer DC.

<b>ICM:</b> The color profile of the DC specified by the <i>hdc</i> parameter will be reset based on the information contained in the <b>lpInitData</b> member of the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/d7f63ef7-0a2e-47c3-9e81-6e8a6dffe9af">DeviceCapabilities</a>



<a href="https://msdn.microsoft.com/ba21b680-78a8-45a2-94e1-01b377b74787">Escape</a>
 

 

