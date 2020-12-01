---
UID: NS:ddrawint._DD_SURFACE_MORE
title: DD_SURFACE_MORE (ddrawint.h)
description: The DD_SURFACE_MORE structure contains additional local data for each individual DirectDrawSurface object.
helpviewer_keywords: ["*PDD_SURFACE_MORE","DD_SURFACE_MORE","DD_SURFACE_MORE structure [Display Devices]","PDD_SURFACE_MORE","PDD_SURFACE_MORE structure pointer [Display Devices]","ddrawint/DD_SURFACE_MORE","ddrawint/PDD_SURFACE_MORE","ddstrcts_b86749f9-edbf-4e8b-ae17-27840ad4e5d5.xml","display.dd_surface_more"]
old-location: display\dd_surface_more.htm
tech.root: display
ms.assetid: 4b000d0f-4ff1-4155-92be-b56793978b1f
ms.date: 12/05/2018
ms.keywords: '*PDD_SURFACE_MORE, DD_SURFACE_MORE, DD_SURFACE_MORE structure [Display Devices], PDD_SURFACE_MORE, PDD_SURFACE_MORE structure pointer [Display Devices], ddrawint/DD_SURFACE_MORE, ddrawint/PDD_SURFACE_MORE, ddstrcts_b86749f9-edbf-4e8b-ae17-27840ad4e5d5.xml, display.dd_surface_more'
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
req.typenames: '*PDD_SURFACE_MORE, DD_SURFACE_MORE'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SURFACE_MORE
 - ddrawint/_DD_SURFACE_MORE
 - PDD_SURFACE_MORE
 - ddrawint/PDD_SURFACE_MORE
 - DD_SURFACE_MORE
 - ddrawint/DD_SURFACE_MORE
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
 - DD_SURFACE_MORE
---

# DD_SURFACE_MORE structure


## -description

The DD_SURFACE_MORE structure contains additional local data for each individual DirectDrawSurface object.

## -struct-fields

### -field dwMipMapCount

Contains the number of mipmap levels in the chain.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure of the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object currently writing data to this surface.

### -field dwOverlayFlags

Specifies a set of flags that indicate the overlay flags most recently passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>. This member is a bitwise OR of any of the following values:

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
Add a dirty rectangle to an emulated overlaid surface.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADEST

</td>
<td>
Use the alpha information in the pixel format or the alpha channel surface attached to the destination surface as the alpha channel for the destination overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTCONSTOVERRIDE

</td>
<td>
Use the <b>dwConstAlphaDest</b> member in the DDOVERLAYFX structure (defined in the Microsoft DirectDraw SDK documentation) as the destination alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTNEG

</td>
<td>
The NEG suffix indicates that the destination surface becomes more transparent as the alpha value increases.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHADESTSURFACEOVERRIDE

</td>
<td>
Use the <b>lpDDSAlphaDest</b> member in the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the alpha channel destination for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHAEDGEBLEND

</td>
<td>
Use the <b>dwAlphaEdgeBlend</b> member in the DDOVERLAYFX structure as the alpha channel for the edges of the image that border the color key colors.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRC

</td>
<td>
Use the alpha information in the pixel format or the alpha channel surface attached to the source surface as the source alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCCONSTOVERRIDE

</td>
<td>
Use the <b>dwConstAlphaSrc</b> member in the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the source alpha channel for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCNEG

</td>
<td>
The NEG suffix indicates that the source surface becomes more transparent as the alpha value increases.

</td>
</tr>
<tr>
<td>
DDOVER_ALPHASRCSURFACEOVERRIDE

</td>
<td>
Use the <b>lpDDSAlphaSrc</b> member in the DDOVERLAYFX structure as the alpha channel source for this overlay.

</td>
</tr>
<tr>
<td>
DDOVER_AUTOFLIP

</td>
<td>
Autoflip the overlay whenever the VPE object autoflips.

</td>
</tr>
<tr>
<td>
DDOVER_BOB

</td>
<td>
Display each field of VPE object data individually without causing any jittery artifacts.

</td>
</tr>
<tr>
<td>
DDOVER_BOBHARDWARE

</td>
<td>
Bob is performed using hardware rather than software or emulated.

</td>
</tr>
<tr>
<td>
DDOVER_DDFX

</td>
<td>
Use the overlay FX flags to define special overlay FX.

</td>
</tr>
<tr>
<td>
DDOVER_HIDE

</td>
<td>
Turn this overlay off.

</td>
</tr>
<tr>
<td>
DDOVER_INTERLEAVED

</td>
<td>
Indicates that the surface memory is composed of interleaved fields.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDEST

</td>
<td>
Use the color key associated with the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYDESTOVERRIDE

</td>
<td>
Use the <b>dckDestColorkey</b> member in the DDOVERLAYFX structure (defined in the DirectDraw SDK documentation) as the color key for the destination surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRC

</td>
<td>
Use the color key associated with the source surface.

</td>
</tr>
<tr>
<td>
DDOVER_KEYSRCOVERRIDE

</td>
<td>
Use the <b>dckSrcColorkey</b> member in the DDOVERLAYFX structure as the color key for the source surface.

</td>
</tr>
<tr>
<td>
DDOVER_OVERRIDEBOBWEAVE

</td>
<td>
Bob and weave decisions should not be overridden by other interfaces. If this flag is set, DirectDraw does not allow a kernel-mode driver to use the kernel-mode video transport functionality to switch the hardware between bob and weave mode.

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHALL

</td>
<td>
Redraw the entire surface on an emulated overlayed surface.

</td>
</tr>
<tr>
<td>
DDOVER_REFRESHDIRTYRECTS

</td>
<td>
Redraw all dirty rectangles on an emulated overlayed surface.

</td>
</tr>
<tr>
<td>
DDOVER_SHOW

</td>
<td>
Turn this overlay on.

</td>
</tr>
</table>

### -field ddsCapsEx

Specifies a DDSCAPSEX structure that is used to expose extended surface capabilities. A DDSCAPSEX structure is the same as a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure without the <b>dwCaps</b> member.

### -field dwSurfaceHandle

Specifies a cookie for <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a> so that it can associate a texture handle with the surface.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurfaceex">D3dCreateSurfaceEx</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_updateoverlay">DdUpdateOverlay</a>