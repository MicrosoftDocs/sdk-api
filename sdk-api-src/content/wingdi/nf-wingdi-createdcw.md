---
UID: NF:wingdi.CreateDCW
title: CreateDCW function (wingdi.h)
description: The CreateDC function creates a device context (DC) for a device using the specified name. (Unicode)
helpviewer_keywords: ["CreateDC", "CreateDC function [Windows GDI]", "CreateDCW", "_win32_CreateDC", "gdi.createdc", "wingdi/CreateDC", "wingdi/CreateDCW"]
old-location: gdi\createdc.htm
tech.root: gdi
ms.assetid: 6fc443c8-da97-4196-a9ed-179a4e583849
ms.date: 12/05/2018
ms.keywords: CreateDC, CreateDC function [Windows GDI], CreateDCA, CreateDCW, _win32_CreateDC, gdi.createdc, wingdi/CreateDC, wingdi/CreateDCA, wingdi/CreateDCW
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDCW
 - wingdi/CreateDCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-Create-l1-1-0.dll
 - Ext-MS-Win-GDI-DC-Create-l1-1-1.dll
 - ext-ms-win-gdi-dc-create-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - CreateDC
 - CreateDCA
 - CreateDCW
---

# CreateDCW function


## -description

The <b>CreateDC</b> function creates a device context (DC) for a device using the specified name.

## -parameters

### -param pwszDriver

A pointer to a null-terminated character string that specifies either DISPLAY or the name of a specific display device. For printing, we recommend that you pass <b>NULL</b> to <i>lpszDriver</i> because GDI ignores <i>lpszDriver</i> for printer devices.

### -param pwszDevice [in]

A pointer to a null-terminated character string that specifies the name of the specific output device being used, as shown by the Print Manager (for example, Epson FX-80). It is not the printer model name. The <i>lpszDevice</i> parameter must be used.

To obtain valid names for displays, call <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesw">EnumDisplayDevices</a>.

If <i>lpszDriver</i> is DISPLAY or the device name of a specific display device, then <i>lpszDevice</i> must be <b>NULL</b> or that same device name. If <i>lpszDevice</i> is <b>NULL</b>, then a DC is created for the primary display device.

If there are multiple monitors on the system, calling <code>CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL)</code> will create a DC covering all the monitors.

### -param pszPort

This parameter is ignored and should be set to <b>NULL</b>. It is provided only for compatibility with 16-bit Windows.

### -param pdm [in]

A pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a> structure containing device-specific initialization data for the device driver. The <a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a> function retrieves this structure filled in for a specified device. The <i>pdm</i> parameter must be <b>NULL</b> if the device driver is to use the default initialization (if any) specified by the user.

If <i>lpszDriver</i> is DISPLAY, <i>pdm</i> must be <b>NULL</b>; GDI then uses the display device's current <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>.

## -returns

If the function succeeds, the return value is the handle to a DC for the specified device.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Note that the handle to the DC can only be used by a single thread at any one time.

For parameters <i>lpszDriver</i> and <i>lpszDevice</i>, call <a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesw">EnumDisplayDevices</a> to obtain valid names for displays.

When you no longer need the DC, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function.

If <i>lpszDriver</i> or <i>lpszDevice</i> is DISPLAY, the thread that calls <b>CreateDC</b> owns the <b>HDC</b> that is created. When this thread is destroyed, the <b>HDC</b> is no longer valid. Thus, if you create the <b>HDC</b> and pass it to another thread, then exit the first thread, the second thread will not be able to use the <b>HDC</b>.

When you call <b>CreateDC</b> to create the <b>HDC</b> for a display device, you must pass to <i>pdm</i> either <b>NULL</b> or a pointer to <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a> that matches the current <b>DEVMODE</b> of the display device that <i>lpszDevice</i> specifies. We recommend to pass <b>NULL</b> and not to try to exactly match the <b>DEVMODE</b> for the current display device.

When you call <b>CreateDC</b> to create the <b>HDC</b> for a printer device, the printer driver validates the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a>. If the printer driver determines that the <b>DEVMODE</b> is invalid (that is, printer driver can’t convert or consume the DEVMODE), the printer driver provides a default <b>DEVMODE</b> to create the HDC for the printer device.

<b>ICM:</b> To enable ICM, set the <b>dmICMMethod</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a> structure (pointed to by the <i>pInitData</i> parameter) to the appropriate value.


#### Examples

For an example, see <a href="/windows/desktop/gdi/capturing-an-image">Capturing an Image</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines CreateDC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-devmodew">DEVMODE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-docinfow">DOCINFO</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/printdocs/documentproperties">DocumentProperties</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enumdisplaydevicesw">EnumDisplayDevices</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-startdocw">StartDoc</a>
