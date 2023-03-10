---
UID: NS:ddrawint.DD_SURFACECALLBACKS
title: DD_SURFACECALLBACKS (ddrawint.h)
description: The DD_SURFACECALLBACKS structure contains entry pointers to the Microsoft DirectDraw surface callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_SURFACECALLBACKS","DD_SURFACECALLBACKS","DD_SURFACECALLBACKS structure [Display Devices]","PDD_SURFACECALLBACKS","PDD_SURFACECALLBACKS structure pointer [Display Devices]","ddrawint/DD_SURFACECALLBACKS","ddrawint/PDD_SURFACECALLBACKS","ddstrcts_868cb884-02fc-4df4-a3ec-1fde158e42b0.xml","display.dd_surfacecallbacks"]
old-location: display\dd_surfacecallbacks.htm
tech.root: display
ms.assetid: a363446e-a9f7-4b32-acc2-c369d3dfe8f3
ms.date: 12/05/2018
ms.keywords: '*PDD_SURFACECALLBACKS, DD_SURFACECALLBACKS, DD_SURFACECALLBACKS structure [Display Devices], PDD_SURFACECALLBACKS, PDD_SURFACECALLBACKS structure pointer [Display Devices], ddrawint/DD_SURFACECALLBACKS, ddrawint/PDD_SURFACECALLBACKS, ddstrcts_868cb884-02fc-4df4-a3ec-1fde158e42b0.xml, display.dd_surfacecallbacks'
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
req.typenames: DD_SURFACECALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_SURFACECALLBACKS
 - ddrawint/DD_SURFACECALLBACKS
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
 - DD_SURFACECALLBACKS
---

# DD_SURFACECALLBACKS structure


## -description

The DD_SURFACECALLBACKS structure contains entry pointers to the Microsoft DirectDraw surface callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of the DD_SURFACECALLBACKS structure. This member is unused by Microsoft Windows 2000 and later versions.

### -field dwFlags

Indicates which DirectDrawSurface callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_SURFCB32_DESTROYSURFACE</dt>
<dt>DDHAL_SURFCB32_FLIP</dt>
<dt>DDHAL_SURFCB32_SETCLIPLIST</dt>
<dt>DDHAL_SURFCB32_LOCK</dt>
<dt>DDHAL_SURFCB32_UNLOCK</dt>
<dt>DDHAL_SURFCB32_BLT</dt>
<dt>DDHAL_SURFCB32_SETCOLORKEY</dt>
<dt>DDHAL_SURFCB32_ADDATTACHEDSURFACE</dt>
<dt>DDHAL_SURFCB32_GETBLTSTATUS</dt>
<dt>DDHAL_SURFCB32_GETFLIPSTATUS</dt>
<dt>DDHAL_SURFCB32_UPDATEOVERLAY</dt>
<dt>DDHAL_SURFCB32_SETOVERLAYPOSITION</dt>
<dt>DDHAL_SURFCB32_SETPALETTE</dt>
</dl>

### -field DestroySurface

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_destroysurface">DdDestroySurface</a> surface callback.

### -field Flip

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a> surface callback.

### -field SetClipList

Points to the driver-supplied <a href="/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide">DdSetClipList</a> surface callback.

### -field Lock

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a> surface callback.

### -field Unlock

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a> surface callback.

### -field Blt

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_blt">DdBlt</a> surface callback.

### -field SetColorKey

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setcolorkey">DdSetColorKey</a> surface callback.

### -field AddAttachedSurface

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_addattachedsurface">DdAddAttachedSurface</a> surface callback.

### -field GetBltStatus

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getbltstatus">DdGetBltStatus</a> surface callback.

### -field GetFlipStatus

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getflipstatus">DdGetFlipStatus</a> surface callback.

### -field UpdateOverlay

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a> surface callback.

### -field SetOverlayPosition

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setoverlayposition">DdSetOverlayPosition</a> surface callback.

### -field reserved4

Reserved for system use and should be ignored by the driver.

### -field SetPalette

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setpalette">DdSetPalette</a> surface callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver initializes this structure in <a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledirectdraw">DrvEnableDirectDraw</a>