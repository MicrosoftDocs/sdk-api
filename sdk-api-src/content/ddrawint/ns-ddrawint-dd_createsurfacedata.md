---
UID: NS:ddrawint._DD_CREATESURFACEDATA
title: DD_CREATESURFACEDATA (ddrawint.h)
description: The DD_CREATESURFACEDATA structure contains information necessary to create a surface--in the case of CreateD3DBuffer, a command or vertex buffer.
helpviewer_keywords: ["*PDD_CREATESURFACEDATA","DD_CREATESURFACEDATA","DD_CREATESURFACEDATA structure [Display Devices]","ddrawint/DD_CREATESURFACEDATA","ddstrcts_bd51b416-f5b7-4a68-833b-7102de67488c.xml","display.dd_createsurfacedata"]
old-location: display\dd_createsurfacedata.htm
tech.root: display
ms.assetid: 5a3b4267-43b4-44dc-abad-cb3f3d07f30e
ms.date: 12/05/2018
ms.keywords: '*PDD_CREATESURFACEDATA, DD_CREATESURFACEDATA, DD_CREATESURFACEDATA structure [Display Devices], ddrawint/DD_CREATESURFACEDATA, ddstrcts_bd51b416-f5b7-4a68-833b-7102de67488c.xml, display.dd_createsurfacedata'
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
req.typenames: '*PDD_CREATESURFACEDATA, DD_CREATESURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CREATESURFACEDATA
 - ddrawint/_DD_CREATESURFACEDATA
 - PDD_CREATESURFACEDATA
 - ddrawint/PDD_CREATESURFACEDATA
 - DD_CREATESURFACEDATA
 - ddrawint/DD_CREATESURFACEDATA
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
 - DD_CREATESURFACEDATA
---

# DD_CREATESURFACEDATA structure


## -description

The DD_CREATESURFACEDATA structure contains information necessary to create a surface--in the case of <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>, a command or vertex buffer.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurfaceDesc

Points to the <a href="/windows/win32/api/ddraw/ns-ddraw-ddsurfacedesc">DDSURFACEDESC</a> structure describing the surface or buffer that the driver should create.

### -field lplpSList

Points to a list of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structures describing the surface objects created by the driver. On Microsoft Windows 2000 and later, there is usually only one entry in this array. However, if the driver supports the Windows 98/Me-style surface creation techniques using <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> with GUID_NTPrivateDriverCaps, and the driver sets the DDHAL_PRIVATECAP_ATOMICSURFACECREATION flag, the member contains a list of surfaces (usually more than one).

### -field dwSCnt

Specifies the number of surfaces in the list to which <b>lplpSList</b> points. This value is usually 1 on Windows 2000 and later. However, if the driver support the Windows 98/Me-style surface creation techniques using <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> with GUID_NTPrivateDriverCaps, the member contains the actual number of surfaces in the list (usually more than one).

### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> or <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field CreateSurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>



<a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>