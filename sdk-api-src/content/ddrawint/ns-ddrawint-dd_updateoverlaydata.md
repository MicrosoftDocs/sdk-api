---
UID: NS:ddrawint._DD_UPDATEOVERLAYDATA
title: DD_UPDATEOVERLAYDATA (ddrawint.h)
description: The DD_UPDATEOVERLAYDATA structure contains information necessary for updating an overlay surface.
helpviewer_keywords: ["*PDD_UPDATEOVERLAYDATA","DD_UPDATEOVERLAYDATA","DD_UPDATEOVERLAYDATA structure [Display Devices]","ddrawint/DD_UPDATEOVERLAYDATA","ddstrcts_43001aad-c6c1-4908-b945-bc612bd7297a.xml","display.dd_updateoverlaydata"]
old-location: display\dd_updateoverlaydata.htm
tech.root: display
ms.assetid: f9dd3fe3-1295-40c8-83d9-74861945921e
ms.date: 12/05/2018
ms.keywords: '*PDD_UPDATEOVERLAYDATA, DD_UPDATEOVERLAYDATA, DD_UPDATEOVERLAYDATA structure [Display Devices], ddrawint/DD_UPDATEOVERLAYDATA, ddstrcts_43001aad-c6c1-4908-b945-bc612bd7297a.xml, display.dd_updateoverlaydata'
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
req.typenames: '*PDD_UPDATEOVERLAYDATA, DD_UPDATEOVERLAYDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_UPDATEOVERLAYDATA
 - ddrawint/_DD_UPDATEOVERLAYDATA
 - PDD_UPDATEOVERLAYDATA
 - ddrawint/PDD_UPDATEOVERLAYDATA
 - DD_UPDATEOVERLAYDATA
 - ddrawint/DD_UPDATEOVERLAYDATA
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
 - DD_UPDATEOVERLAYDATA
---

# DD_UPDATEOVERLAYDATA structure


## -description

The DD_UPDATEOVERLAYDATA structure contains information necessary for updating an overlay surface.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDDestSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that represents the Microsoft DirectDraw surface to be overlaid. This value can be <b>NULL</b> if DDOVER_HIDE is specified in <b>dwFlags</b>.

### -field rDest

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that contains the x, y, width, and height of the region on the destination surface to be overlaid.

### -field lpDDSrcSurface

Points to a DD_SURFACE_LOCAL structure that describes the overlay surface.

### -field rSrc

Specifies a RECTL structure that contains the x, y, width, and height of the region on the source surface to be used for the overlay.

### -field dwFlags

Specifies how the driver should handle the overlay. This member can be a combination of any of the following flags: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDOVER_ADDDIRTYRECT

</td>
<td>
Should be ignored by the driver.

</td>
</tr>
<tr>
<td>
DDOVER_AUTOFLIP

</td>
<td>
The driver should autoflip the overlay whenever the hardware video port autoflips. Drivers that support <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> need only check this flag.

</td>
</tr>
<tr>
<td>
DDOVER_BOB

</td>
<td>
The driver should display each field of VPE object data individually without causing any jittery artifacts. This flag pertains to both VPE and decoders that want to do their own flipping in kernel mode using the kernel-mode video transport functionality.

</td>
</tr>
<tr>
<td>
DDOVER_BOBHARDWARE

</td>
<td>
Indicates that bob is performed by hardware rather than by software or emulation. Drivers that support VPE need only check this flag.

</td>
</tr>
<tr>
<td>
DDOVER_DDFX

</td>
<td>
The driver should show the overlay surface using the attributes specified by the <b>overlayFX</b> member.

</td>
</tr>
<tr>
<td>
DDOVER_HIDE

</td>
<td>
The driver should hide the overlay; that is, the driver should turn this overlay off.

</td>
</tr>
<tr>
<td>
DDOVER_INTERLEAVED

</td>
<td>
The overlay surface is composed of interleaved fields. Drivers that support VPE need only check this flag.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDEST

</td>
<td>
The driver should use the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDESTOVERRIDE

</td>
<td>
The driver should use the <b>dckDestColorKey</b> member of the DDOVERLAYFX structure (described in the DirectDraw SDK documentation) as the destination color key instead of the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRC

</td>
<td>
The driver should use the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRCOVERRIDE

</td>
<td>
The driver should use the <b>dckSrcColorKey</b> member of the DDOVERLAYFX structure (described in the DirectDraw SDK documentation) as the source color key instead of the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_OVERRIDEBOBWEAVE

</td>
<td>
Bob/weave decisions should not be overridden by other interfaces. If the overlay mixer sets this flag, DirectDraw does not allow a kernel-mode driver to use the kernel-mode video transport functionality to switch the hardware between bob and weave mode. 

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHALL

</td>
<td>
Should be ignored by the driver.

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHDIRTYRECTS

</td>
<td>
Should be ignored by the driver.

</td>
</tr>
<tr>
<td>
DDOVER_SHOW

</td>
<td>
The driver should show the overlay; that is, the driver should turn this overlay on.

</td>
</tr>
</table>

### -field overlayFX

Specifies a DDOVERLAYFX structure (described in the DirectDraw SDK documentation) that describes additional effects that the driver should use to update the overlay. The driver should use this structure only if one of DDOVER_DDFX, DDOVER_KEYDESTOVERRIDE, or DDOVER_KEYSRCOVERRIDE are set in the <b>dwFlags</b> member.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field UpdateOverlay

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>