---
UID: NS:ddkmapi._DDGETSURFACESTATEOUT
title: DDGETSURFACESTATEOUT (ddkmapi.h)
description: The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface.
helpviewer_keywords: ["*LPDDGETSURFACESTATEOUT","DDGETSURFACESTATEOUT","DDGETSURFACESTATEOUT structure [Display Devices]","LPDDGETSURFACESTATEOUT","LPDDGETSURFACESTATEOUT structure pointer [Display Devices]","ddkmapi/DDGETSURFACESTATEOUT","ddkmapi/LPDDGETSURFACESTATEOUT","ddstrcts_bfeeac46-f803-48ee-aac4-39cb4781f925.xml","display.ddgetsurfacestateout"]
old-location: display\ddgetsurfacestateout.htm
tech.root: display
ms.assetid: 8d84fcdf-c880-4a3e-a57d-12bb8e59cb5b
ms.date: 12/05/2018
ms.keywords: '*LPDDGETSURFACESTATEOUT, DDGETSURFACESTATEOUT, DDGETSURFACESTATEOUT structure [Display Devices], LPDDGETSURFACESTATEOUT, LPDDGETSURFACESTATEOUT structure pointer [Display Devices], ddkmapi/DDGETSURFACESTATEOUT, ddkmapi/LPDDGETSURFACESTATEOUT, ddstrcts_bfeeac46-f803-48ee-aac4-39cb4781f925.xml, display.ddgetsurfacestateout'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDGETSURFACESTATEOUT, *LPDDGETSURFACESTATEOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDGETSURFACESTATEOUT
 - ddkmapi/_DDGETSURFACESTATEOUT
 - LPDDGETSURFACESTATEOUT
 - ddkmapi/LPDDGETSURFACESTATEOUT
 - DDGETSURFACESTATEOUT
 - ddkmapi/DDGETSURFACESTATEOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDGETSURFACESTATEOUT
---

# DDGETSURFACESTATEOUT structure


## -description

The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface.

## -struct-fields

### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function for <a href="/previous-versions/windows/hardware/drivers/ff550673(v=vs.85)">DD_DXAPI_GET_SURFACE_STATE</a> operations. A return code of DD_OK indicates success.

### -field dwStateCaps

Contains the DirectDrawSurface's capabilities of the device. One or more of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSTATE_BOB

</td>
<td>
The device is capable of performing bob mode.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
The device is capable of performing weave mode.

</td>
</tr>
</table>

### -field dwStateStatus

Contains the status of the selected DirectDrawSurface. One or more of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSTATE_BOB

</td>
<td>
Bob mode is being used on this surface.

</td>
</tr>
<tr>
<td>
DDSTATE_EXPLICITLY_SET

</td>
<td>
This state is due to a previous <a href="/previous-versions/windows/hardware/drivers/ff551504(v=vs.85)">DD_DXAPI_SET_SURFACE_STATE</a> call.

</td>
</tr>
<tr>
<td>
DDSTATE_SKIPEVENFIELDS

</td>
<td>
Stop bob or weave mode and skip every other field instead.

</td>
</tr>
<tr>
<td>
DDSTATE_SOFTWARE_AUTOFLIP

</td>
<td>
Software (as opposed to hardware) autoflipping is being used.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
Weave mode is being used on this surface.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550673(v=vs.85)">DD_DXAPI_GET_SURFACE_STATE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>