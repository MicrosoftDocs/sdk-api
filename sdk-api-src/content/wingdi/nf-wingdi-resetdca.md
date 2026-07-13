---
UID: NF:wingdi.ResetDCA
title: ResetDCA function (wingdi.h)
description: The ResetDC function updates the specified printer or plotter device context (DC) using the specified information. (ANSI)
helpviewer_keywords: ["ResetDCA", "wingdi/ResetDCA"]
old-location: gdi\resetdc.htm
tech.root: gdi
ms.assetid: 3f77db51-90d1-4a87-812b-1e129ae8fde9
ms.date: 12/05/2018
ms.keywords: ResetDC, ResetDC function [Windows GDI], ResetDCA, ResetDCW, _win32_ResetDC, gdi.resetdc, wingdi/ResetDC, wingdi/ResetDCA, wingdi/ResetDCW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResetDCA
 - wingdi/ResetDCA
dev_langs:
 - c++
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
---

# ResetDCA function


## -description

The <b>ResetDC</b> function updates the specified printer or plotter device context (DC) using the specified information.

## -parameters

### -param hdc [in]

A handle to the DC to update.

### -param lpdm [in]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure containing information about the new DC.

## -returns

If the function succeeds, the return value is a handle to the original DC.

If the function fails, the return value is <b>NULL</b>.

## -remarks

An application will typically use the <b>ResetDC</b> function when a window receives a <a href="/windows/desktop/gdi/wm-devmodechange">WM_DEVMODECHANGE</a> message. <b>ResetDC</b> can also be used to change the paper orientation or paper bins while printing a document.

The <b>ResetDC</b> function cannot be used to change the driver name, device name, or the output port. When the user changes the port connection or device name, the application must delete the original DC and create a new DC with the new information.

An application can pass an information DC to the <b>ResetDC</b> function. In that situation, <b>ResetDC</b> will always return a printer DC.

<b>ICM:</b> The color profile of the DC specified by the <i>hdc</i> parameter will be reset based on the information contained in the <b>lpInitData</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure.





> [!NOTE]
> The wingdi.h header defines ResetDC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa">DeviceCapabilities</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-escape">Escape</a>
