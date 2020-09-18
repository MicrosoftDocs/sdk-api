---
UID: NS:ddrawint._DD_FLIPTOGDISURFACEDATA
title: DD_FLIPTOGDISURFACEDATA (ddrawint.h)
description: The DD_FLIPTOGDISURFACEDATA structure contains the GDI surface notification information.
helpviewer_keywords: ["*PDD_FLIPTOGDISURFACEDATA","DD_FLIPTOGDISURFACEDATA","DD_FLIPTOGDISURFACEDATA structure [Display Devices]","ddrawint/DD_FLIPTOGDISURFACEDATA","ddstrcts_7e93a017-4f74-43c9-9aaa-6e64da35870d.xml","display.dd_fliptogdisurfacedata"]
old-location: display\dd_fliptogdisurfacedata.htm
tech.root: display
ms.assetid: ac0fdaf7-0cb2-4474-b3dd-a039161513a4
ms.date: 12/05/2018
ms.keywords: '*PDD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA structure [Display Devices], ddrawint/DD_FLIPTOGDISURFACEDATA, ddstrcts_7e93a017-4f74-43c9-9aaa-6e64da35870d.xml, display.dd_fliptogdisurfacedata'
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
req.typenames: '*PDD_FLIPTOGDISURFACEDATA, DD_FLIPTOGDISURFACEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_FLIPTOGDISURFACEDATA
 - ddrawint/_DD_FLIPTOGDISURFACEDATA
 - PDD_FLIPTOGDISURFACEDATA
 - ddrawint/PDD_FLIPTOGDISURFACEDATA
 - DD_FLIPTOGDISURFACEDATA
 - ddrawint/DD_FLIPTOGDISURFACEDATA
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
 - DD_FLIPTOGDISURFACEDATA
---

# DD_FLIPTOGDISURFACEDATA structure


## -description

The DD_FLIPTOGDISURFACEDATA structure contains the GDI surface notification information.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field dwToGDI

Indicates that Microsoft DirectDraw is flipping to a GDI surface when <b>TRUE</b>; indicates that DirectDraw is flipping from a GDI surface when <b>FALSE</b>.

### -field dwReserved

Reserved for system use and should be ignored by the driver.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_fliptogdisurface">DdFlipToGDISurface</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field FlipToGDISurface

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_fliptogdisurface">DdFlipToGDISurface</a>