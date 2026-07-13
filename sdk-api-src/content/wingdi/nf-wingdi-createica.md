---
UID: NF:wingdi.CreateICA
title: CreateICA function (wingdi.h)
description: The CreateIC function creates an information context for the specified device. (ANSI)
helpviewer_keywords: ["CreateICA", "wingdi/CreateICA"]
old-location: gdi\createic.htm
tech.root: gdi
ms.assetid: dcb08ce7-9ded-497c-936c-48d3026a0004
ms.date: 12/05/2018
ms.keywords: CreateIC, CreateIC function [Windows GDI], CreateICA, CreateICW, _win32_CreateIC, gdi.createic, wingdi/CreateIC, wingdi/CreateICA, wingdi/CreateICW
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateICA
 - wingdi/CreateICA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
 - ext-ms-win-gdi-dc-create-l1-1-2.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateIC
 - CreateICA
 - CreateICW
---

# CreateICA function


## -description

The <b>CreateIC</b> function creates an information context for the specified device. The information context provides a fast way to get information about the device without creating a device context (DC). However, GDI drawing functions cannot accept a handle to an information context.

## -parameters

### -param pszDriver [in]

A pointer to a null-terminated character string that specifies the name of the device driver (for example, Epson).

### -param pszDevice [in]

A pointer to a null-terminated character string that specifies the name of the specific output device being used, as shown by the Print Manager (for example, Epson FX-80). It is not the printer model name. The <i>lpszDevice</i> parameter must be used.

### -param pszPort

This parameter is ignored and should be set to <b>NULL</b>. It is provided only for compatibility with 16-bit Windows.

### -param pdm [in]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure containing device-specific initialization data for the device driver. The <a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a> function retrieves this structure filled in for a specified device. The <i>lpdvmInit</i> parameter must be <b>NULL</b> if the device driver is to use the default initialization (if any) specified by the user.

## -returns

If the function succeeds, the return value is the handle to an information context.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the information DC, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function.





> [!NOTE]
> The wingdi.h header defines CreateIC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>
