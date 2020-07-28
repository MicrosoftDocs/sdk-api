---
UID: NF:winddi.EngMarkBandingSurface
title: EngMarkBandingSurface function (winddi.h)
description: The EngMarkBandingSurface function marks the specified surface as a banding surface.
helpviewer_keywords: ["EngMarkBandingSurface","EngMarkBandingSurface function [Display Devices]","display.engmarkbandingsurface","gdifncs_b597b27e-e521-40ec-a16f-7961b64dead2.xml","winddi/EngMarkBandingSurface"]
old-location: display\engmarkbandingsurface.htm
tech.root: display
ms.assetid: 0ee3d697-42aa-4117-9d85-63472e4a042f
ms.date: 12/05/2018
ms.keywords: EngMarkBandingSurface, EngMarkBandingSurface function [Display Devices], display.engmarkbandingsurface, gdifncs_b597b27e-e521-40ec-a16f-7961b64dead2.xml, winddi/EngMarkBandingSurface
f1_keywords:
- winddi/EngMarkBandingSurface
dev_langs:
- c++
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- EngMarkBandingSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngMarkBandingSurface function


## -description


The <b>EngMarkBandingSurface </b>function marks the specified surface as a banding surface.


## -parameters




### -param hsurf [in]

Caller-supplied handle to the surface to mark as a banding surface.


## -returns



<b>EngMarkBandingSurface</b> returns <b>TRUE</b> upon success; otherwise it returns <b>FALSE</b>.




## -remarks



If a <a href="https://docs.microsoft.com/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> uses GDI-managed surfaces, it must call <b>EngMarkBandingSurface</b> if it cannot create a surface (by calling <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>) that is large enough to hold an entire physical page's bitmap. Both <b>EngCreateBitmap</b> and <b>EngMarkBandingSurface</b> should be called from within the printer graphics DLL's <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a> function.

The handle supplied for <i>hsurf</i> must be a bitmap handle returned by <b>EngCreateBitmap</b>.

If a printer graphics DLL calls <b>EngMarkBandingSurface</b>, it must define <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvstartbanding">DrvStartBanding</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a> functions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvstartbanding">DrvStartBanding</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>
 

 

