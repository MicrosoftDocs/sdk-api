---
UID: NS:ddrawint._DD_GETVPORTFLIPSTATUSDATA
title: DD_GETVPORTFLIPSTATUSDATA (ddrawint.h)
description: The DD_GETVPORTFLIPSTATUSDATA structure contains the flip status information for the specified surface.
helpviewer_keywords: ["*PDD_GETVPORTFLIPSTATUSDATA","DD_GETVPORTFLIPSTATUSDATA","DD_GETVPORTFLIPSTATUSDATA structure [Display Devices]","ddrawint/DD_GETVPORTFLIPSTATUSDATA","ddstrcts_a1239418-1670-477d-b96e-d21dc2b9647b.xml","display.dd_getvportflipstatusdata"]
old-location: display\dd_getvportflipstatusdata.htm
tech.root: display
ms.assetid: 64be9019-a75f-42db-a636-b767f87c1858
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA structure [Display Devices], ddrawint/DD_GETVPORTFLIPSTATUSDATA, ddstrcts_a1239418-1670-477d-b96e-d21dc2b9647b.xml, display.dd_getvportflipstatusdata'
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
req.typenames: '*PDD_GETVPORTFLIPSTATUSDATA, DD_GETVPORTFLIPSTATUSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTFLIPSTATUSDATA
 - ddrawint/_DD_GETVPORTFLIPSTATUSDATA
 - PDD_GETVPORTFLIPSTATUSDATA
 - ddrawint/PDD_GETVPORTFLIPSTATUSDATA
 - DD_GETVPORTFLIPSTATUSDATA
 - ddrawint/DD_GETVPORTFLIPSTATUSDATA
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
 - DD_GETVPORTFLIPSTATUSDATA
---

# DD_GETVPORTFLIPSTATUSDATA structure


## -description

The DD_GETVPORTFLIPSTATUSDATA structure contains the flip status information for the specified surface.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field fpSurface

Points to the surface for which the flip status information is required.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getflipstatus">DdVideoPortGetFlipStatus</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortFlipStatus

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getflipstatus">DdVideoPortGetFlipStatus</a>