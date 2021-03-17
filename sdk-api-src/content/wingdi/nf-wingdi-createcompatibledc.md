---
UID: NF:wingdi.CreateCompatibleDC
title: CreateCompatibleDC function (wingdi.h)
description: The CreateCompatibleDC function creates a memory device context (DC) compatible with the specified device.
helpviewer_keywords: ["CreateCompatibleDC","CreateCompatibleDC function [Windows GDI]","_win32_CreateCompatibleDC","gdi.createcompatibledc","wingdi/CreateCompatibleDC"]
old-location: gdi\createcompatibledc.htm
tech.root: gdi
ms.assetid: 6ddc3705-2995-41af-af94-258aed597e17
ms.date: 12/05/2018
ms.keywords: CreateCompatibleDC, CreateCompatibleDC function [Windows GDI], _win32_CreateCompatibleDC, gdi.createcompatibledc, wingdi/CreateCompatibleDC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateCompatibleDC
 - wingdi/CreateCompatibleDC
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
 - CreateCompatibleDC
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

A memory DC exists only in memory. When the memory DC is created, its display surface is exactly one monochrome pixel wide and one monochrome pixel high. Before an application can use a memory DC for drawing operations, it must select a bitmap of the correct width and height into the DC. To select a bitmap into a DC, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a> function, specifying the height, width, and color organization required.

When a memory DC is created, all attributes are set to normal default values. The memory DC can be used as a normal DC. You can set the attributes; obtain the current settings of its attributes; and select pens, brushes, and regions.

The <b>CreateCompatibleDC</b> function can only be used with devices that support raster operations. An application can determine whether a device supports these operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function.

When you no longer need the memory DC, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a> function. We recommend that you call <b>DeleteDC</b> to delete the DC.  However, you can also call <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> with the HDC to delete the DC.

If <i>hdc</i> is <b>NULL</b>, the thread that calls <b>CreateCompatibleDC</b> owns the HDC that is created. When this thread is destroyed, the HDC is no longer valid. Thus, if you create the HDC and pass it to another thread, then exit the first thread, the second thread will not be able to use the HDC.

<b>ICM:</b> If the DC that is passed to this function is enabled for Image Color Management (ICM), the DC created by the function is ICM-enabled. The source and destination color spaces are specified in the DC.


#### Examples

For an example, see <a href="/windows/desktop/gdi/capturing-an-image">Capturing an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deletedc">DeleteDC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>