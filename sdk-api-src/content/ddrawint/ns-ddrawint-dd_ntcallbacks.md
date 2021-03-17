---
UID: NS:ddrawint._DD_NTCALLBACKS
title: DD_NTCALLBACKS (ddrawint.h)
description: The DD_NTCALLBACKS structure contains entry pointers to Microsoft Windows 2000 and later Microsoft DirectDraw callback functions that a device driver supports.
helpviewer_keywords: ["*PDD_NTCALLBACKS","DD_NTCALLBACKS","DD_NTCALLBACKS structure [Display Devices]","PDD_NTCALLBACKS","PDD_NTCALLBACKS structure pointer [Display Devices]","ddrawint/DD_NTCALLBACKS","ddrawint/PDD_NTCALLBACKS","ddstrcts_1e79e318-f193-455c-b4c6-5f016b539207.xml","display.dd_ntcallbacks"]
old-location: display\dd_ntcallbacks.htm
tech.root: display
ms.assetid: 9d226b1c-6959-4cc8-9e60-b57a324d9a8a
ms.date: 12/05/2018
ms.keywords: '*PDD_NTCALLBACKS, DD_NTCALLBACKS, DD_NTCALLBACKS structure [Display Devices], PDD_NTCALLBACKS, PDD_NTCALLBACKS structure pointer [Display Devices], ddrawint/DD_NTCALLBACKS, ddrawint/PDD_NTCALLBACKS, ddstrcts_1e79e318-f193-455c-b4c6-5f016b539207.xml, display.dd_ntcallbacks'
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
req.typenames: DD_NTCALLBACKS, *PDD_NTCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_NTCALLBACKS
 - ddrawint/_DD_NTCALLBACKS
 - PDD_NTCALLBACKS
 - ddrawint/PDD_NTCALLBACKS
 - DD_NTCALLBACKS
 - ddrawint/DD_NTCALLBACKS
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
 - DD_NTCALLBACKS
---

# DD_NTCALLBACKS structure


## -description

The DD_NTCALLBACKS structure contains entry pointers to Microsoft Windows 2000 and later Microsoft DirectDraw callback functions that a device driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_NTCALLBACKS structure.

### -field dwFlags

Indicates what Windows 2000 and later callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_NTCB32_FREEDRIVERMEMORY</dt>
<dt>DDHAL_NTCB32_SETEXCLUSIVEMODE</dt>
<dt>DDHAL_NTCB32_FLIPTOGDISURFACE</dt>
</dl>

### -field FreeDriverMemory

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_freedrivermemory">DdFreeDriverMemory</a> callback.

### -field SetExclusiveMode

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_setexclusivemode">DdSetExclusiveMode</a> callback.

### -field FlipToGDISurface

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_fliptogdisurface">DdFlipToGDISurface</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_NTCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_fliptogdisurface">DdFlipToGDISurface</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_freedrivermemory">DdFreeDriverMemory</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_setexclusivemode">DdSetExclusiveMode</a>