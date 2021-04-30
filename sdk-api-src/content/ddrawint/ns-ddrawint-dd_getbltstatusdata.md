---
UID: NS:ddrawint._DD_GETBLTSTATUSDATA
title: DD_GETBLTSTATUSDATA (ddrawint.h)
description: The DD_GETBLTSTATUSDATA structure returns the blit status information.
helpviewer_keywords: ["*PDD_GETBLTSTATUSDATA","DD_GETBLTSTATUSDATA","DD_GETBLTSTATUSDATA structure [Display Devices]","ddrawint/DD_GETBLTSTATUSDATA","ddstrcts_fec10d7e-ffc0-4368-8cd8-e1028ac7874d.xml","display.dd_getbltstatusdata"]
old-location: display\dd_getbltstatusdata.htm
tech.root: display
ms.assetid: 16b0cac9-af8c-4106-b74e-6c9ada543851
ms.date: 12/05/2018
ms.keywords: '*PDD_GETBLTSTATUSDATA, DD_GETBLTSTATUSDATA, DD_GETBLTSTATUSDATA structure [Display Devices], ddrawint/DD_GETBLTSTATUSDATA, ddstrcts_fec10d7e-ffc0-4368-8cd8-e1028ac7874d.xml, display.dd_getbltstatusdata'
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
req.typenames: '*PDD_GETBLTSTATUSDATA, DD_GETBLTSTATUSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETBLTSTATUSDATA
 - ddrawint/_DD_GETBLTSTATUSDATA
 - PDD_GETBLTSTATUSDATA
 - ddrawint/PDD_GETBLTSTATUSDATA
 - DD_GETBLTSTATUSDATA
 - ddrawint/DD_GETBLTSTATUSDATA
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
 - DD_GETBLTSTATUSDATA
---

# DD_GETBLTSTATUSDATA structure


## -description

The DD_GETBLTSTATUSDATA structure returns the blit status information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure representing the surface whose blit status is being queried.

### -field dwFlags

Specifies the blit status being requested. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDGBS_CANBLT

</td>
<td>
Queries whether the driver can currently perform a blit.

</td>
</tr>
<tr>
<td>
DDGBS_ISBLTDONE

</td>
<td>
Queries whether the driver has completed the last blit.

</td>
</tr>
</table>

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getbltstatus">DdGetBltStatus</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetBltStatus

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_getbltstatus">DdGetBltStatus</a>