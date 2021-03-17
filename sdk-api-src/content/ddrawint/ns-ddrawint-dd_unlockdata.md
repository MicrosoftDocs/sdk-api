---
UID: NS:ddrawint._DD_UNLOCKDATA
title: DD_UNLOCKDATA (ddrawint.h)
description: The DD_UNLOCKDATA structure contains information necessary to do an unlock as defined by Microsoft DirectDraw parameter structures.
helpviewer_keywords: ["*PDD_UNLOCKDATA","DD_UNLOCKDATA","DD_UNLOCKDATA structure [Display Devices]","ddrawint/DD_UNLOCKDATA","ddstrcts_1784fe3c-5a41-4428-ac94-06226857ae9a.xml","display.dd_unlockdata"]
old-location: display\dd_unlockdata.htm
tech.root: display
ms.assetid: 4642f596-376f-4f63-bf6e-916112ce1ec9
ms.date: 12/05/2018
ms.keywords: '*PDD_UNLOCKDATA, DD_UNLOCKDATA, DD_UNLOCKDATA structure [Display Devices], ddrawint/DD_UNLOCKDATA, ddstrcts_1784fe3c-5a41-4428-ac94-06226857ae9a.xml, display.dd_unlockdata'
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
req.typenames: '*PDD_UNLOCKDATA, DD_UNLOCKDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_UNLOCKDATA
 - ddrawint/_DD_UNLOCKDATA
 - PDD_UNLOCKDATA
 - ddrawint/PDD_UNLOCKDATA
 - DD_UNLOCKDATA
 - ddrawint/DD_UNLOCKDATA
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
 - DD_UNLOCKDATA
---

# DD_UNLOCKDATA structure


## -description

The DD_UNLOCKDATA structure contains information necessary to do an unlock as defined by Microsoft DirectDraw parameter structures.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface--in the case of <a href="/previous-versions/windows/hardware/drivers/ff570106(v=vs.85)">UnlockD3DBuffer</a>, a buffer--to be unlocked.

### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a> or <a href="/previous-versions/windows/hardware/drivers/ff570106(v=vs.85)">UnlockD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field Unlock

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a>



<a href="/previous-versions/windows/hardware/drivers/ff570106(v=vs.85)">UnlockD3DBuffer</a>