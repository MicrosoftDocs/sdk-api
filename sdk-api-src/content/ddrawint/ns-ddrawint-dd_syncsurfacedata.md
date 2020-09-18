---
UID: NS:ddrawint._DD_SYNCSURFACEDATA
title: DD_SYNCSURFACEDATA (ddrawint.h)
description: The DD_SYNCSURFACEDATA structure contains the surface information.
helpviewer_keywords: ["*PDD_SYNCSURFACEDATA","DD_SYNCSURFACEDATA","DD_SYNCSURFACEDATA structure [Display Devices]","PDD_SYNCSURFACEDATA","PDD_SYNCSURFACEDATA structure pointer [Display Devices]","ddrawint/DD_SYNCSURFACEDATA","ddrawint/PDD_SYNCSURFACEDATA","ddstrcts_59fb70d7-7462-48bf-a0f7-3d54cdf8f62e.xml","display.dd_syncsurfacedata"]
old-location: display\dd_syncsurfacedata.htm
tech.root: display
ms.assetid: 76294b03-9182-408a-a0ee-1a24f8b53163
ms.date: 12/05/2018
ms.keywords: '*PDD_SYNCSURFACEDATA, DD_SYNCSURFACEDATA, DD_SYNCSURFACEDATA structure [Display Devices], PDD_SYNCSURFACEDATA, PDD_SYNCSURFACEDATA structure pointer [Display Devices], ddrawint/DD_SYNCSURFACEDATA, ddrawint/PDD_SYNCSURFACEDATA, ddstrcts_59fb70d7-7462-48bf-a0f7-3d54cdf8f62e.xml, display.dd_syncsurfacedata'
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
req.typenames: '*PDD_SYNCSURFACEDATA, DD_SYNCSURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SYNCSURFACEDATA
 - ddrawint/_DD_SYNCSURFACEDATA
 - PDD_SYNCSURFACEDATA
 - ddrawint/PDD_SYNCSURFACEDATA
 - DD_SYNCSURFACEDATA
 - ddrawint/DD_SYNCSURFACEDATA
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
 - DD_SYNCSURFACEDATA
---

# DD_SYNCSURFACEDATA structure


## -description

The DD_SYNCSURFACEDATA structure contains the surface information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpDDSurface

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface with which to sync.

### -field dwSurfaceOffset

Contains the byte offset from the start of the frame buffer to the start of the surface. This value is used only by the video miniport driver. This member must contain data that is filled in by the driver.

### -field fpLockPtr

Contains the pointer value to be returned by the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a> call for accessing the surface. This value is used by a kernel-mode client. This member can be modified by the driver, but does not need to be.

### -field lPitch

Contains the pitch in bytes passed to the client during a <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a> call. This member can be modified by the driver, but does not need to be.

### -field dwOverlayOffset

Contains the byte offset from the start of the frame buffer to the start of the overlay. This value is used only by the video miniport driver and may be different than the <b>dwSurfaceOffset</b> member if cropping is involved or if the overlay origin is not the top left of the surface. This member must contain data that is filled in by the driver.

### -field dwDriverReserved1

Reserved for use by the display driver.

### -field dwDriverReserved2

Reserved for use by the display driver.

### -field dwDriverReserved3

Reserved for use by the display driver.

### -field dwDriverReserved4

Reserved for use by the display driver. Windows 2000 and later only.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncsurface">DdSyncSurfaceData</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_kernelcb_syncsurface">DdSyncSurfaceData</a>