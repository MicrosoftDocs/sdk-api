---
UID: NS:ddrawint._DD_ADDATTACHEDSURFACEDATA
title: DD_ADDATTACHEDSURFACEDATA (ddrawint.h)
description: The DD_ADDATTACHEDSURFACEDATA structure contains information necessary to attach a surface to another surface.
helpviewer_keywords: ["*PDD_ADDATTACHEDSURFACEDATA","DD_ADDATTACHEDSURFACEDATA","DD_ADDATTACHEDSURFACEDATA structure [Display Devices]","ddrawint/DD_ADDATTACHEDSURFACEDATA","ddstrcts_2697c197-c588-4f30-8f96-db7d835f3929.xml","display.dd_addattachedsurfacedata"]
old-location: display\dd_addattachedsurfacedata.htm
tech.root: display
ms.assetid: d00120d9-5825-4998-a1ef-ccc5654b91b9
ms.date: 12/05/2018
ms.keywords: '*PDD_ADDATTACHEDSURFACEDATA, DD_ADDATTACHEDSURFACEDATA, DD_ADDATTACHEDSURFACEDATA structure [Display Devices], ddrawint/DD_ADDATTACHEDSURFACEDATA, ddstrcts_2697c197-c588-4f30-8f96-db7d835f3929.xml, display.dd_addattachedsurfacedata'
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
req.typenames: '*PDD_ADDATTACHEDSURFACEDATA, DD_ADDATTACHEDSURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_ADDATTACHEDSURFACEDATA
 - ddrawint/_DD_ADDATTACHEDSURFACEDATA
 - PDD_ADDATTACHEDSURFACEDATA
 - ddrawint/PDD_ADDATTACHEDSURFACEDATA
 - DD_ADDATTACHEDSURFACEDATA
 - ddrawint/DD_ADDATTACHEDSURFACEDATA
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
 - DD_ADDATTACHEDSURFACEDATA
---

# DD_ADDATTACHEDSURFACEDATA structure


## -description

The DD_ADDATTACHEDSURFACEDATA structure contains information necessary to attach a surface to another surface.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that represents the surface to which another surface is being attached.

### -field lpSurfAttached

Points to a DD_SURFACE_LOCAL structure that represents the surface to be attached.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_addattachedsurface">DdAddAttachedSurface</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field AddAttachedSurface

Unused on Microsoft Windows 2000 and later.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_addattachedsurface">DdAddAttachedSurface</a>