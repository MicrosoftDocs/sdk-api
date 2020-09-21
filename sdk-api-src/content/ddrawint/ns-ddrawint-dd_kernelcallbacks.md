---
UID: NS:ddrawint.DD_KERNELCALLBACKS
title: DD_KERNELCALLBACKS (ddrawint.h)
description: The DD_KERNELCALLBACKS structure contains entry pointers to the DirectDraw kernel-mode callback functions that the driver supports.
helpviewer_keywords: ["*PDD_KERNELCALLBACKS","DD_KERNELCALLBACKS","DD_KERNELCALLBACKS structure [Display Devices]","PDD_KERNELCALLBACKS","PDD_KERNELCALLBACKS structure pointer [Display Devices]","ddrawint/DD_KERNELCALLBACKS","ddrawint/PDD_KERNELCALLBACKS","ddstrcts_6d33c1f1-37e3-421a-b40f-1009a5ee3d25.xml","display.dd_kernelcallbacks"]
old-location: display\dd_kernelcallbacks.htm
tech.root: display
ms.assetid: 85dcb71b-ad1f-4b83-8ead-db502d9f294e
ms.date: 12/05/2018
ms.keywords: '*PDD_KERNELCALLBACKS, DD_KERNELCALLBACKS, DD_KERNELCALLBACKS structure [Display Devices], PDD_KERNELCALLBACKS, PDD_KERNELCALLBACKS structure pointer [Display Devices], ddrawint/DD_KERNELCALLBACKS, ddrawint/PDD_KERNELCALLBACKS, ddstrcts_6d33c1f1-37e3-421a-b40f-1009a5ee3d25.xml, display.dd_kernelcallbacks'
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
req.typenames: DD_KERNELCALLBACKS, *PDD_KERNELCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_KERNELCALLBACKS
 - ddrawint/DD_KERNELCALLBACKS
 - PDD_KERNELCALLBACKS
 - ddrawint/PDD_KERNELCALLBACKS
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
 - DD_KERNELCALLBACKS
---

# DD_KERNELCALLBACKS structure


## -description

The DD_KERNELCALLBACKS structure contains entry pointers to the DirectDraw kernel-mode callback functions that the driver supports.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_KERNELCALLBACKS structure.

### -field dwFlags

Indicates what Microsoft DirectDraw kernel callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_KERNEL_SYNCSURFACEDATA </dt>
<dt>DDHAL_KERNEL_SYNCVIDEOPORTDATA </dt>
</dl>

### -field SyncSurfaceData

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncsurface">DdSyncSurfaceData</a> callback.

### -field SyncVideoPortData

Points to the driver-supplied <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncvideoport">DdSyncVideoPortData</a> callback.

## -remarks

Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_KernelCallbacks GUID.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncsurface">DdSyncSurfaceData</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncvideoport">DdSyncVideoPortData</a>