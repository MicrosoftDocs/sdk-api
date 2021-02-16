---
UID: NS:ddrawint._DD_SETCOLORKEYDATA
title: DD_SETCOLORKEYDATA (ddrawint.h)
description: The DD_SETCOLORKEYDATA structure contains information necessary to set the color key value for the specified surface.
helpviewer_keywords: ["*PDD_SETCOLORKEYDATA","DD_SETCOLORKEYDATA","DD_SETCOLORKEYDATA structure [Display Devices]","ddrawint/DD_SETCOLORKEYDATA","ddstrcts_2798d2f9-38f8-42c3-a28e-a0d2a2ac3433.xml","display.dd_setcolorkeydata"]
old-location: display\dd_setcolorkeydata.htm
tech.root: display
ms.assetid: 08d17ac7-a5d4-47ed-9ee4-896471b46769
ms.date: 12/05/2018
ms.keywords: '*PDD_SETCOLORKEYDATA, DD_SETCOLORKEYDATA, DD_SETCOLORKEYDATA structure [Display Devices], ddrawint/DD_SETCOLORKEYDATA, ddstrcts_2798d2f9-38f8-42c3-a28e-a0d2a2ac3433.xml, display.dd_setcolorkeydata'
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
req.typenames: '*PDD_SETCOLORKEYDATA, DD_SETCOLORKEYDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SETCOLORKEYDATA
 - ddrawint/_DD_SETCOLORKEYDATA
 - PDD_SETCOLORKEYDATA
 - ddrawint/PDD_SETCOLORKEYDATA
 - DD_SETCOLORKEYDATA
 - ddrawint/DD_SETCOLORKEYDATA
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
 - DD_SETCOLORKEYDATA
---

# DD_SETCOLORKEYDATA structure


## -description

The DD_SETCOLORKEYDATA structure contains information necessary to set the color key value for the specified surface.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface with which the color key is to be associated.

### -field dwFlags

Specifies which color key is being requested. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDCKEY_COLORSPACE

</td>
<td>
The DDCOLORKEY structure contains a color space. If this bit is not set, the structure contains a single color key.

</td>
</tr>
<tr>
<td>
DDCKEY_DESTBLT

</td>
<td>
The DDCOLORKEY structure specifies a color key or color space to be used as a destination color key for blt operations.

</td>
</tr>
<tr>
<td>
DDCKEY_DESTOVERLAY

</td>
<td>
The DDCOLORKEY structure specifies a color key or color space to be used as a destination color key for overlay operations.

</td>
</tr>
<tr>
<td>
DDCKEY_SRCBLT

</td>
<td>
The DDCOLORKEY structure specifies a color key or color space to be used as a source color key for blit operations.

</td>
</tr>
<tr>
<td>
DDCKEY_SRCOVERLAY

</td>
<td>
The DDCOLORKEY structure specifies a color key or color space to be used as a source color key for overlay operations

</td>
</tr>
</table>

### -field ckNew

Specifies a DDCOLORKEY structure that specifies the new color key values for the DirectDrawSurface object. For more information about DDCOLORKEY, see the latest Microsoft DirectX SDK documentation.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setcolorkey">DdSetColorKey</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field SetColorKey

This is not used on Microsoft Windows 2000 and later.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setcolorkey">DdSetColorKey</a>