---
UID: NS:ddrawint._DD_CREATESURFACEEXDATA
title: DD_CREATESURFACEEXDATA (ddrawint.h)
description: The DD_CREATESURFACEEXDATA structure contains information required for the driver to create a surface and associate with it a supplied texture handle.
helpviewer_keywords: ["*PDD_CREATESURFACEEXDATA","DD_CREATESURFACEEXDATA","DD_CREATESURFACEEXDATA structure [Display Devices]","d3dstrct_221c1055-03a3-4b43-bef4-8b0fbd6eb45e.xml","ddrawint/DD_CREATESURFACEEXDATA","display.dd_createsurfaceexdata"]
old-location: display\dd_createsurfaceexdata.htm
tech.root: display
ms.assetid: 61965d6b-7473-4121-8c85-fb677a665388
ms.date: 12/05/2018
ms.keywords: '*PDD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA structure [Display Devices], d3dstrct_221c1055-03a3-4b43-bef4-8b0fbd6eb45e.xml, ddrawint/DD_CREATESURFACEEXDATA, display.dd_createsurfaceexdata'
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
req.typenames: '*PDD_CREATESURFACEEXDATA, DD_CREATESURFACEEXDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CREATESURFACEEXDATA
 - ddrawint/_DD_CREATESURFACEEXDATA
 - PDD_CREATESURFACEEXDATA
 - ddrawint/PDD_CREATESURFACEEXDATA
 - DD_CREATESURFACEEXDATA
 - ddrawint/DD_CREATESURFACEEXDATA
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
 - DD_CREATESURFACEEXDATA
---

# DD_CREATESURFACEEXDATA structure


## -description

The DD_CREATESURFACEEXDATA structure contains information required for the driver to create a surface and associate with it a supplied texture handle.

## -struct-fields

### -field dwFlags

Specifies a set of flags for the <b>D3dCreateSurfaceEx</b> function that are currently not used and always zero.

### -field lpDDLcl

Specifies a handle to the DirectDraw object created by the application. This is the scope within which the <b>lpDDSLcl</b> handles exist. A <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure describes the driver.

### -field lpDDSLcl

Specifies a handle to the DirectDraw surface to be created for Direct3D. These handles are unique within each different DD_DIRECTDRAW_LOCAL structure. A <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure represents the created surface object.

### -field ddRVal

Specifies the location where the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a> callback. A return code of D3D_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-codes-for-direct3d-driver-callbacks">Return Codes for Direct3D Driver Callbacks</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>