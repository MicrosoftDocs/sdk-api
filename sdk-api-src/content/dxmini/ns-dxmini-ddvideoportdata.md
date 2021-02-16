---
UID: NS:dxmini.DDVIDEOPORTDATA
title: DDVIDEOPORTDATA (dxmini.h)
description: The DDVIDEOPORTDATA structure is used by DirectDraw to represent a video port extensions (VPE) object to the kernel-mode video miniport driver.
helpviewer_keywords: ["*LPDDVIDEOPORTDATA","DDVIDEOPORTDATA","DDVIDEOPORTDATA structure [Display Devices]","LPDDVIDEOPORTDATA","LPDDVIDEOPORTDATA structure pointer [Display Devices]","Video_Structs_2c27c41d-7b5c-4e72-a362-ca2699099ef4.xml","display.ddvideoportdata","dxmini/DDVIDEOPORTDATA","dxmini/LPDDVIDEOPORTDATA"]
old-location: display\ddvideoportdata.htm
tech.root: display
ms.assetid: 662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df
ms.date: 12/05/2018
ms.keywords: '*LPDDVIDEOPORTDATA, DDVIDEOPORTDATA, DDVIDEOPORTDATA structure [Display Devices], LPDDVIDEOPORTDATA, LPDDVIDEOPORTDATA structure pointer [Display Devices], Video_Structs_2c27c41d-7b5c-4e72-a362-ca2699099ef4.xml, display.ddvideoportdata, dxmini/DDVIDEOPORTDATA, dxmini/LPDDVIDEOPORTDATA'
req.header: dxmini.h
req.include-header: Dxmini.h
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
req.typenames: DDVIDEOPORTDATA, *LPDDVIDEOPORTDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DDVIDEOPORTDATA
 - dxmini/DDVIDEOPORTDATA
 - LPDDVIDEOPORTDATA
 - dxmini/LPDDVIDEOPORTDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDVIDEOPORTDATA
---

# DDVIDEOPORTDATA structure


## -description

The DDVIDEOPORTDATA structure is used by DirectDraw to represent a <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object to the kernel-mode video miniport driver.

## -struct-fields

### -field dwVideoPortId

Specifies the ID of this hardware video port, an integer in the range (0 - (maximum number of hardware video ports - 1)).

### -field dwVPFlags

Indicates a set of flags that specify the current user mode DDVP_<i>Xxx</i> flags set by <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a>. This member can be a bitwise OR of any of the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVP_AUTOFLIP

</td>
<td>
Perform automatic flipping. Autoflipping is performed between the overlay surface that was attached to the hardware video port using the application's <b>AttachSurface</b> method, and the overlay surfaces that are attached to the surface using the application's <b>AttachSurface</b> method. The flip order is the order in which the overlay surfaces were attached.

</td>
</tr>
<tr>
<td>
DDVP_CONVERT

</td>
<td>
Perform the conversion using the target surface format.

</td>
</tr>
<tr>
<td>
DDVP_CROP

</td>
<td>
Perform cropping using the specified rectangle.

</td>
</tr>
<tr>
<td>
DDVP_HARDWAREDEINTERLACE

</td>
<td>
The hardware video port should use the deinterlacing hardware.

</td>
</tr>
<tr>
<td>
DDVP_IGNOREVBIXCROP

</td>
<td>
The video data should ignore the left and right cropping coordinates when cropping the <a href="/windows-hardware/drivers/">vertical blanking interval (VBI)</a> data.

</td>
</tr>
<tr>
<td>
DDVP_INTERLEAVE

</td>
<td>
Interlaced fields should be interleaved in memory.

</td>
</tr>
<tr>
<td>
DDVP_MIRRORLEFTRIGHT

</td>
<td>
The data should be mirrored left to right as it is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVP_MIRRORUPDOWN

</td>
<td>
The data should be mirrored top to bottom as it is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVP_OVERRIDEBOBWEAVE

</td>
<td>
These bob and weave decisions should not be overridden by other interfaces. If this flag is set, DirectDraw does not allow a kernel-mode driver to use the kernel-mode video transport functionality to switch the hardware between bob and weave modes.

</td>
</tr>
<tr>
<td>
DDVP_PRESCALE

</td>
<td>
Perform prescaling/zooming based on the prescale parameters.

</td>
</tr>
<tr>
<td>
DDVP_SKIPEVENFIELDS

</td>
<td>
Ignore input of even fields.

</td>
</tr>
<tr>
<td>
DDVP_SKIPODDFIELDS

</td>
<td>
Ignore input of odd fields.

</td>
</tr>
<tr>
<td>
DDVP_SYNCMASTER

</td>
<td>
Drive the graphics V-syncs using the hardware video port V-syncs.

</td>
</tr>
<tr>
<td>
DDVP_VBICONVERT

</td>
<td>
The <b>lpddpfVBIOutputFormat</b> member contains data that should be used to convert the data within the vertical blanking interval.

</td>
</tr>
<tr>
<td>
DDVP_VBINOINTERLEAVE

</td>
<td>
Interleaving can be disabled for data within the vertical blanking interval.

</td>
</tr>
<tr>
<td>
DDVP_VBINOSCALE

</td>
<td>
Data within the vertical blanking interval should not be scaled.

</td>
</tr>
</table>

### -field dwOriginOffset

Specifies the byte offset of the VPE object relative to the start of the surface. This value is used only by the miniport driver.

### -field dwHeight

Specifies the height in pixels of the VPE object data. This value is used only by the miniport driver.

### -field dwVBIHeight

Specifies the height in scan lines of the VBI data. This value is used only by the miniport driver.

### -field dwDriverReserved1

Reserved for use by the miniport driver.

### -field dwDriverReserved2

Reserved for use by the miniport driver.

### -field dwDriverReserved3

Reserved for use by the miniport driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_update">DdVideoPortUpdate</a>