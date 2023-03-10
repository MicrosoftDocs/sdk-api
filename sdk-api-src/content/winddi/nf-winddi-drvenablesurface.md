---
UID: NF:winddi.DrvEnableSurface
title: DrvEnableSurface function (winddi.h)
description: The DrvEnableSurface function sets up a surface to be drawn on and associates it with a given physical device.
helpviewer_keywords: ["DrvEnableSurface","DrvEnableSurface function [Display Devices]","ddifncs_c0044970-ac75-4dae-af55-f6fd87079dbb.xml","display.drvenablesurface","winddi/DrvEnableSurface"]
old-location: display\drvenablesurface.htm
tech.root: display
ms.assetid: a838a44a-243c-4d0d-bda3-eec9a626cb53
ms.date: 12/05/2018
ms.keywords: DrvEnableSurface, DrvEnableSurface function [Display Devices], ddifncs_c0044970-ac75-4dae-af55-f6fd87079dbb.xml, display.drvenablesurface, winddi/DrvEnableSurface
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvEnableSurface
 - winddi/DrvEnableSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvEnableSurface
---

# DrvEnableSurface function


## -description

The <b>DrvEnableSurface</b> function sets up a surface to be drawn on and associates it with a given physical device.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a>. This is the return value of <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>. The PDEV describes the physical device for which a surface is to be created.

## -returns

The return value is a handle that identifies the newly created surface. Otherwise, it is zero, and an error code is logged.

## -remarks

There are two methods for preparing a surface for use. 

<ol>
<li>
In this method, which is recommended, the driver creates the surface by a call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicesurface">EngCreateDeviceSurface</a>. After GDI creates the surface and returns a handle to the driver, the driver calls <a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a>, which sets the appropriate hook flags, and optionally, informs GDI of the surface's location.

</li>
<li>
The second method is the one used by Windows NT 4.0 drivers. In this method, the driver calls <a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>. After this call, the driver calls <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a> to associate the surface with the physical display device. This GDI function allows the driver to specify which graphics output routines are supported for standard-format bitmaps. A call to this function can be made only when no surface exists for the given physical device. If a Windows 2000 or later driver is back-ported to run on Windows NT 4.0, this method must be used. If such a driver will also run on Windows 2000 or later, a separate code path in the driver should use the first method. 

For printer devices, the usual situation is for GDI to collect the graphics directly onto a GDI bitmap. The driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>, which allows GDI to allocate memory for the bitmap.

</li>
</ol>
Any existing GDI bitmap handle is a valid surface handle.

For <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLLs</a> that use GDI-managed surfaces, the <b>DrvEnableSurface</b> function should call <a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>, specifying a surface size large enough to contain an entire physical page. If that fails, repeated calls to <b>EngCreateBitmap</b> should be attempted, with decreasing surface sizes, until a call succeeds. The valid size should be specified as input to <a href="/windows/desktop/api/winddi/nf-winddi-engmarkbandingsurface">EngMarkBandingSurface</a>, which informs GDI that surface banding will be necessary.

After <b>DrvEnableSurface</b> returns a handle to a primary surface, do not call <a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="https://support.microsoft.com/?kbid&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.

<b>DrvEnableSurface</b> is required for graphics drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdisablesurface">DrvDisableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicesurface">EngCreateDeviceSurface</a>