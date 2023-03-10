---
UID: NS:ddrawint.DD_CALLBACKS
title: DD_CALLBACKS (ddrawint.h)
description: The DD_CALLBACKS structure contains entry pointers to the callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_CALLBACKS","DD_CALLBACKS","DD_CALLBACKS structure [Display Devices]","ddrawint/DD_CALLBACKS","ddstrcts_c4da6934-e140-40db-b7dc-686c205cb877.xml","display.dd_callbacks"]
old-location: display\dd_callbacks.htm
tech.root: display
ms.assetid: d68b2772-dca6-417a-8e03-d3b2843fb69d
ms.date: 12/05/2018
ms.keywords: '*PDD_CALLBACKS, DD_CALLBACKS, DD_CALLBACKS structure [Display Devices], ddrawint/DD_CALLBACKS, ddstrcts_c4da6934-e140-40db-b7dc-686c205cb877.xml, display.dd_callbacks'
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: DD_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_CALLBACKS
 - ddrawint/DD_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_CALLBACKS
---

# DD_CALLBACKS structure


## -description

The DD_CALLBACKS structure contains entry pointers to the callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this structure.

### -field dwFlags

Indicates what Microsoft DirectDraw callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_CB32_CANCREATESURFACE</dt>
<dt>DDHAL_CB32_CREATEPALETTE</dt>
<dt>DDHAL_CB32_CREATESURFACE</dt>
<dt>DDHAL_CB32_GETSCANLINE</dt>
<dt>DDHAL_CB32_MAPMEMORY</dt>
<dt>DDHAL_CB32_SETCOLORKEY</dt>
<dt>DDHAL_CB32_SETMODE</dt>
<dt>DDHAL_CB32_WAITFORVERTICALBLANK</dt>
</dl>

### -field DestroyDriver

Unused on Microsoft Windows 2000 and later and should be ignored by the driver.

### -field CreateSurface

Points to the driver-supplied <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> callback.

### -field SetColorKey

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setcolorkey">DdSetColorKey</a> callback.

### -field SetMode

Unused on Windows 2000 and later and should be ignored by the driver.

### -field WaitForVerticalBlank

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_waitforverticalblank">DdWaitForVerticalBlank</a> callback.

### -field CanCreateSurface

Points to the driver-supplied <a href="/previous-versions/windows/hardware/drivers/ff549213(v=vs.85)">DdCanCreateSurface</a> callback.

### -field CreatePalette

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createpalette">DdCreatePalette</a> callback.

### -field GetScanLine

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getscanline">DdGetScanLine</a> callback.

### -field MapMemory

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mapmemory">DdMapMemory</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. GDI allocates the memory for this structure and calls the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a> function to initialize it.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>