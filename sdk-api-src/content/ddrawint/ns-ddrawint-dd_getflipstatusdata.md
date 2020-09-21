---
UID: NS:ddrawint._DD_GETFLIPSTATUSDATA
title: DD_GETFLIPSTATUSDATA (ddrawint.h)
description: The DD_GETFLIPSTATUSDATA structure returns the flip status information.
helpviewer_keywords: ["*PDD_GETFLIPSTATUSDATA","DD_GETFLIPSTATUSDATA","DD_GETFLIPSTATUSDATA structure [Display Devices]","ddrawint/DD_GETFLIPSTATUSDATA","ddstrcts_03291da8-7881-46a2-8b11-291124a5732d.xml","display.dd_getflipstatusdata"]
old-location: display\dd_getflipstatusdata.htm
tech.root: display
ms.assetid: da3b90e0-1a60-434b-966c-a7ebabff33ee
ms.date: 12/05/2018
ms.keywords: '*PDD_GETFLIPSTATUSDATA, DD_GETFLIPSTATUSDATA, DD_GETFLIPSTATUSDATA structure [Display Devices], ddrawint/DD_GETFLIPSTATUSDATA, ddstrcts_03291da8-7881-46a2-8b11-291124a5732d.xml, display.dd_getflipstatusdata'
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
req.typenames: '*PDD_GETFLIPSTATUSDATA, DD_GETFLIPSTATUSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETFLIPSTATUSDATA
 - ddrawint/_DD_GETFLIPSTATUSDATA
 - PDD_GETFLIPSTATUSDATA
 - ddrawint/PDD_GETFLIPSTATUSDATA
 - DD_GETFLIPSTATUSDATA
 - ddrawint/DD_GETFLIPSTATUSDATA
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
 - DD_GETFLIPSTATUSDATA
---

# DD_GETFLIPSTATUSDATA structure


## -description

The DD_GETFLIPSTATUSDATA structure returns the flip status information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface whose flip status is being queried.

### -field dwFlags

Specifies the flip status being requested. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDGFS_CANFLIP

</td>
<td>
Queries whether the driver can currently perform a flip.

</td>
</tr>
<tr>
<td>
DDGFS_ISFLIPDONE

</td>
<td>
Queries whether the driver has finished the last flip.

</td>
</tr>
</table>

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getflipstatus">DdGetFlipStatus</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetFlipStatus

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getflipstatus">DdGetFlipStatus</a>