---
UID: NS:dvp._DDVIDEOPORTINFO
title: DDVIDEOPORTINFO (dvp.h)
description: The DDVIDEOPORTINFO structure describes how the driver should transfer video data to a surface (or to surfaces); DDVIDEOPORTINFO is a member of the DD_VIDEOPORT_LOCAL structure.
helpviewer_keywords: ["*LPDDVIDEOPORTINFO","DDVIDEOPORTINFO","DDVIDEOPORTINFO structure [Display Devices]","ddstrcts_7190df68-6789-4dd1-8cbf-697a863435c5.xml","display.ddvideoportinfo","dvp/DDVIDEOPORTINFO"]
old-location: display\ddvideoportinfo.htm
tech.root: display
ms.assetid: 65423d9e-d3b8-4545-8afe-09b3375dbac2
ms.date: 12/05/2018
ms.keywords: '*LPDDVIDEOPORTINFO, DDVIDEOPORTINFO, DDVIDEOPORTINFO structure [Display Devices], ddstrcts_7190df68-6789-4dd1-8cbf-697a863435c5.xml, display.ddvideoportinfo, dvp/DDVIDEOPORTINFO'
req.header: dvp.h
req.include-header: Dvp.h
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
req.typenames: '*LPDDVIDEOPORTINFO, DDVIDEOPORTINFO'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDVIDEOPORTINFO
 - dvp/_DDVIDEOPORTINFO
 - LPDDVIDEOPORTINFO
 - dvp/LPDDVIDEOPORTINFO
 - DDVIDEOPORTINFO
 - dvp/DDVIDEOPORTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvp.h
api_name:
 - DDVIDEOPORTINFO
---

# DDVIDEOPORTINFO structure


## -description

The DDVIDEOPORTINFO structure describes how the driver should transfer video data to a surface (or to surfaces); DDVIDEOPORTINFO is a member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure.

## -struct-fields

### -field dwSize

Specifies the size in bytes of the structure. This member must be initialized before the structure is used.

### -field dwOriginX

Indicates the x placement of the video data within the surface, in pixels. This offset applies to all surfaces when autoflipping is requested.

### -field dwOriginY

Indicates the y placement of the video data within the surface, in pixels. This offset applies to all surfaces when autoflipping is requested.

### -field dwVPFlags

Indicates a set of flags that specify how the driver should transfer the video data. This member can be a bitwise OR of the following values:

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
Perform automatic flipping. Auto-flipping is performed between the overlay surface that was attached to the hardware video port and the overlay surfaces that are attached to the surface. The flip order is the order in which the overlay surfaces were attached.

</td>
</tr>
<tr>
<td>
DDVP_CONVERT

</td>
<td>
The video data and target surface have different formats. The driver should convert the video data to the format of the target surface format.

</td>
</tr>
<tr>
<td>
DDVP_CROP

</td>
<td>
The driver should crop both the video and <a href="/windows-hardware/drivers/">VBI</a> data using the rectangle in the <b>rCrop</b> member.

</td>
</tr>
<tr>
<td>
DDVP_IGNOREVBIXCROP

</td>
<td>
The driver should ignore the left and right cropping coordinates when cropping the VBI data.

</td>
</tr>
<tr>
<td>
DDVP_INTERLEAVE

</td>
<td>
Interlaced fields of both video and VBI data should be interleaved in memory.

</td>
</tr>
<tr>
<td>
DDVP_MIRRORLEFTRIGHT

</td>
<td>
Video data should be mirrored left to right as it is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVP_MIRRORUPDOWN

</td>
<td>
Video data should be mirrored top to bottom as it is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVP_NOINTERLEAVE

</td>
<td>
If the DDVP_INTERLEAVE flag is set, the driver should interleave the video data only; that is, the driver should not interleave the VBI data.

</td>
</tr>
<tr>
<td>
DDVP_OVERRIDEBOBWEAVE

</td>
<td>
The bob and weave decisions should not be overridden by other interfaces. If this flag is set, Microsoft DirectDraw does not allow a kernel-mode driver to use the kernel-mode video transport functionality to switch the hardware between bob and weave modes.

</td>
</tr>
<tr>
<td>
DDVP_PRESCALE

</td>
<td>
Perform prescaling/zooming based on the <b>dwPrescaleWidth</b> and <b>dwPrescaleHeight</b> members. The driver should prescale only the video data if DDVP_VBINOSCALE is set; otherwise, it should prescale both the video and VBI data.

</td>
</tr>
<tr>
<td>
DDVP_SKIPEVENFIELDS

</td>
<td>
Ignore input of even fields for both video and VBI data.

</td>
</tr>
<tr>
<td>
DDVP_SKIPODDFIELDS

</td>
<td>
Ignore input of odd fields for both video and VBI data.

</td>
</tr>
<tr>
<td>
DDVP_SYNCMASTER

</td>
<td>
Drive the graphics VSYNCs using the hardware video port VSYNCs.

</td>
</tr>
<tr>
<td>
DDVP_VBICONVERT

</td>
<td>
The <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure to which the <b>lpddpfVBIOutputFormat</b> member points contains data that should be used to convert the data within the vertical blanking interval.

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

### -field rCrop

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies a cropping rectangle in pixels. This member contains a valid rectangle when the DDVP_CROP flag is set in the <b>dwVPFlags</b> member.

### -field dwPrescaleWidth

Specifies the width in pixels to which the video and VBI data should be prescaled or zoomed. For example, if the video data is 720 pixels wide and the client requests the width cut in half, the client specifies 360 in <b>dwPrescaleWidth</b>. This member contains a valid width when the DDVP_PRESCALE flag is set in the <b>dwVPFlags</b> member.

### -field dwPrescaleHeight

Specifies the height in pixels to which the video and VBI data should be prescaled or zoomed. For example, if the video data is 240 pixels wide and the client requests the width cut in half, the client specifies 120 in <b>dwPrescaleHeight</b>. This member contains a valid width when the DDVP_PRESCALE flag is set in the <b>dwVPFlags</b> member.

### -field lpddpfInputFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that specifies the format of the video data to be written to the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object. This format can be different from the target surface format if the VPE object performs a conversion.

### -field lpddpfVBIInputFormat

Points to a DDPIXELFORMAT structure that specifies the input format of the data within the vertical blanking interval.

### -field lpddpfVBIOutputFormat

Points to a DDPIXELFORMAT structure that specifies the output format of the data within the vertical blanking interval.

### -field dwVBIHeight

Specifies the number of lines of data within the vertical blanking interval.

### -field dwReserved1

Reserved for system use and should be ignored by the driver.

### -field dwReserved2

Reserved for system use and should be ignored by the driver.

## -remarks

All members of this structure are set by the client and the driver should never change them. The client is typically the overlay mixer.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a>