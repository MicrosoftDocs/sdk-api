---
UID: NS:ddrawint._DD_CANCREATESURFACEDATA
title: DD_CANCREATESURFACEDATA (ddrawint.h)
description: The DD_CANCREATESURFACEDATA structure contains information necessary to indicate whether a surface--in the case of CanCreateD3DBuffer, a buffer--can be created.
helpviewer_keywords: ["*PDD_CANCREATESURFACEDATA","DD_CANCREATESURFACEDATA","DD_CANCREATESURFACEDATA structure [Display Devices]","ddrawint/DD_CANCREATESURFACEDATA","ddstrcts_53ef5031-d754-4aab-8729-520852df024a.xml","display.dd_cancreatesurfacedata"]
old-location: display\dd_cancreatesurfacedata.htm
tech.root: display
ms.assetid: 35ac7efd-1949-497c-8730-2c4414aed977
ms.date: 12/05/2018
ms.keywords: '*PDD_CANCREATESURFACEDATA, DD_CANCREATESURFACEDATA, DD_CANCREATESURFACEDATA structure [Display Devices], ddrawint/DD_CANCREATESURFACEDATA, ddstrcts_53ef5031-d754-4aab-8729-520852df024a.xml, display.dd_cancreatesurfacedata'
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
req.typenames: '*PDD_CANCREATESURFACEDATA, DD_CANCREATESURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CANCREATESURFACEDATA
 - ddrawint/_DD_CANCREATESURFACEDATA
 - PDD_CANCREATESURFACEDATA
 - ddrawint/PDD_CANCREATESURFACEDATA
 - DD_CANCREATESURFACEDATA
 - ddrawint/DD_CANCREATESURFACEDATA
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
 - DD_CANCREATESURFACEDATA
---

# DD_CANCREATESURFACEDATA structure


## -description

The DD_CANCREATESURFACEDATA structure contains information necessary to indicate whether a surface--in the case of <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a>, a buffer--can be created.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurfaceDesc

Points to a <a href="/windows/win32/api/ddraw/ns-ddraw-ddsurfacedesc">DDSURFACEDESC</a> structure that contains a description of the surface or buffer to be created. See the Remarks section for additional information about this member.

### -field bIsDifferentPixelFormat

Indicates whether the pixel format of the surface to be created differs from that of the primary surface. For the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a> D3DBuffer callback, this member is always set to <b>FALSE</b> because the driver is attempting to create a buffer that contains vertex data or commands, rather than pixel data.

### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="/previous-versions/windows/hardware/drivers/ff549213(v=vs.85)">DdCanCreateSurface</a> or <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field CanCreateSurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -remarks

The DirectDraw surface description pointed to by the <b>lpDDSurfaceDesc</b> member is actually a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure (rather than a DDSURFACEDESC structure) for DirectDraw 6.0 and later runtimes. Therefore, if you need information at surface-creation time from those members that are in the DDSURFACEDESC2 structure but not in the DDSURFACEDESC structure, you can simply cast the pointer to a DDSURFACEDESC structure to a pointer to a DDSURFACEDESC2 structure prior to use. The following example shows how the value of <b>dwTextureStage</b> (a member of the DDSURFACEDESC2 structure, but not also of the DDSURFACEDESC structure) can be obtained from a pointer to a DDSURFACEDESC structure.


```
DDSURFACEDESC2* pddsd = (DDSURFACEDESC2*)pccsd->lpDDSurfaceDesc;
DWORD dwStage = pddsd->dwTextureStage;
```

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a>



<a href="/previous-versions/windows/hardware/drivers/ff549213(v=vs.85)">DdCanCreateSurface</a>