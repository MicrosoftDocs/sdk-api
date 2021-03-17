---
UID: NS:dvp._DDVIDEOPORTCAPS
title: DDVIDEOPORTCAPS (dvp.h)
description: The DDVIDEOPORTCAPS structure describes the capabilities and alignment restrictions of a hardware video port.
helpviewer_keywords: ["*LPDDVIDEOPORTCAPS","DDVIDEOPORTCAPS","DDVIDEOPORTCAPS structure [Display Devices]","ddstrcts_6955b71e-772c-41a5-9aa0-7d0247fc9d0a.xml","display.ddvideoportcaps","dvp/DDVIDEOPORTCAPS"]
old-location: display\ddvideoportcaps.htm
tech.root: display
ms.assetid: ea85f189-7308-48ad-b159-1809749f8183
ms.date: 12/05/2018
ms.keywords: '*LPDDVIDEOPORTCAPS, DDVIDEOPORTCAPS, DDVIDEOPORTCAPS structure [Display Devices], ddstrcts_6955b71e-772c-41a5-9aa0-7d0247fc9d0a.xml, display.ddvideoportcaps, dvp/DDVIDEOPORTCAPS'
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
req.typenames: '*LPDDVIDEOPORTCAPS, DDVIDEOPORTCAPS'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDVIDEOPORTCAPS
 - dvp/_DDVIDEOPORTCAPS
 - LPDDVIDEOPORTCAPS
 - dvp/LPDDVIDEOPORTCAPS
 - DDVIDEOPORTCAPS
 - dvp/DDVIDEOPORTCAPS
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
 - DDVIDEOPORTCAPS
---

# DDVIDEOPORTCAPS structure


## -description

The DDVIDEOPORTCAPS structure describes the capabilities and alignment restrictions of a hardware video port.

## -struct-fields

### -field dwSize

Specifies the size in bytes of the structure.

### -field dwFlags

Specify what members in this structure contain valid data. This member can be a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPD_ALIGN

</td>
<td>

<dl>
<dt>All of the alignment members are valid. These include:</dt>
<dt><b>dwAlignVideoPortBoundary</b>,</dt>
<dt><b>dwAlignVideoPortPrescaleWidth</b>,</dt>
<dt><b>dwAlignVideoPortCropBoundary</b>, and </dt>
<dt><b>dwAlignVideoPortCropWidth</b>.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDVPD_AUTOFLIP

</td>
<td>
The <b>dwNumAutoFlipSurfaces</b> is valid.

</td>
</tr>
<tr>
<td>
DDVPD_CAPS

</td>
<td>
The <b>dwCaps</b> member is valid.

</td>
</tr>
<tr>
<td>
DDVPD_FX

</td>
<td>
The <b>dwFX</b> member is valid.

</td>
</tr>
<tr>
<td>
DDVPD_HEIGHT

</td>
<td>
The <b>dwMaxHeight</b> member is valid.

</td>
</tr>
<tr>
<td>
DDVPD_ID

</td>
<td>
The <b>dwVideoPortID</b> member is valid.

</td>
</tr>
<tr>
<td>
DDVPD_WIDTH

</td>
<td>
The <b>dwMaxWidth</b> and <b>dwMaxVBIWidth</b> members are valid.

</td>
</tr>
</table>

### -field dwMaxWidth

Specifies the maximum field width in pixels supported by the hardware video port. This value is typically dictated by the number of bits in the width register.

### -field dwMaxVBIWidth

Specifies the maximum width, in number of samples, in a line of <a href="/windows-hardware/drivers/">VBI</a> data supported by the hardware video port. This value can be larger than the normal field width if the hardware video port supports oversampled VBI data.

### -field dwMaxHeight

Specifies the maximum field height in pixels supported by the hardware video port. This value is typically dictated by the number of bits in the height register.

### -field dwVideoPortID

Specifies the hardware video port ID for this entry. This member should be the index number of this DDVIDEOPORTCAPS structure within the array to which the <b>lpDDVideoPortCaps</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure points. This value ranges from 0 to (<b>dwMaxVideoPorts</b> - 1). (<b>dwMaxVideoPorts</b> is a member of the <a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a> structure.) If the device supports only one hardware video port, this member should be zero.

### -field dwCaps

Indicates a set of flags that specify the capabilities supported by this hardware video port. This member can be a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPCAPS_AUTOFLIP

</td>
<td>
A flip can be performed automatically to avoid tearing.

</td>
</tr>
<tr>
<td>
DDVPCAPS_COLORCONTROL

</td>
<td>
The hardware video port can perform color operations on the incoming data before it is written to the frame buffer.

</td>
</tr>
<tr>
<td>
DDVPCAPS_INTERLACED

</td>
<td>
The hardware video port supports interlaced video.

</td>
</tr>
<tr>
<td>
DDVPCAPS_NONINTERLACED

</td>
<td>
The hardware video port supports noninterlaced video.

</td>
</tr>
<tr>
<td>
DDVPCAPS_OVERSAMPLEDVBI

</td>
<td>
The hardware video port can accept VBI data in a different width or format than the regular video data.

</td>
</tr>
<tr>
<td>
DDVPCAPS_READBACKFIELD

</td>
<td>
The device can return a value signifying whether the current field of an interlaced signal is even or odd.

</td>
</tr>
<tr>
<td>
DDVPCAPS_READBACKLINE

</td>
<td>
The device can return the number of the current line of video being written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVPCAPS_SHAREABLE

</td>
<td>
Ignored by Microsoft DirectDraw.

</td>
</tr>
<tr>
<td>
DDVPCAPS_SKIPEVENFIELDS

</td>
<td>
The hardware video port can automatically discard even fields of video.

</td>
</tr>
<tr>
<td>
DDVPCAPS_SKIPODDFIELDS

</td>
<td>
The hardware video port can automatically discard odd fields of video.

</td>
</tr>
<tr>
<td>
DDVPCAPS_SYNCMASTER

</td>
<td>
The device is capable of driving the graphics V-sync with the hardware video port driver V-sync.

</td>
</tr>
<tr>
<td>
DDVPCAPS_SYSTEMMEMORY

</td>
<td>
The hardware video port can write data directly to system memory.

</td>
</tr>
<tr>
<td>
DDVPCAPS_VBISURFACE

</td>
<td>
The data within the vertical blanking interval can be written to a different surface.

</td>
</tr>
</table>

### -field dwFX

Indicates a set of flags that specify the effects supported by this hardware video port. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPFX_CROPTOPDATA

</td>
<td>
The hardware video port supports limited cropping to crop out the vertical interval data.

</td>
</tr>
<tr>
<td>
DDVPFX_CROPX

</td>
<td>
The hardware video port can crop incoming data in the x direction before writing it to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_CROPY

</td>
<td>
The hardware video port can crop incoming data in the y direction before writing it to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_IGNOREVBIXCROP

</td>
<td>
The hardware video port can ignore the left and right cropping coordinates for video data when cropping oversampled VBI data.

</td>
</tr>
<tr>
<td>
DDVPFX_INTERLEAVE

</td>
<td>
The hardware video port supports interleaving interlaced fields in memory.

</td>
</tr>
<tr>
<td>
DDVPFX_MIRRORLEFTRIGHT

</td>
<td>
The hardware video port supports mirroring left to right as the video data is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVPFX_MIRRORUPDOWN

</td>
<td>
The hardware video port supports mirroring top to bottom as the video data is written into the frame buffer.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKX

</td>
<td>
Data can be arbitrarily shrunk in the x direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKXB

</td>
<td>
Data can be shrunk by negative powers of 2 (1/2, 1/4, 1/8, and so on) in the x direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKXS

</td>
<td>
Data can be shrunk in increments of 1/<b>dwPreshrinkXStep</b> in the x direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKY

</td>
<td>
Data can be arbitrarily shrunk in the y direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKYB

</td>
<td>
Data can be shrunk by negative powers of 2 (1/2, 1/4, 1/8, and so on) in the y direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESHRINKYS

</td>
<td>
Data can be shrunk in increments of 1/<b>dwPreshrinkYStep</b> in the y direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESTRETCHX

</td>
<td>
Data can be arbitrarily stretched in the x direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESTRETCHXN

</td>
<td>
Data can be stretched by integer factors in the x direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESTRETCHY

</td>
<td>
Data can be arbitrarily stretched in the y direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_PRESTRETCHYN

</td>
<td>
Data can be stretched by integer factors in the y direction before it is written to the surface.

</td>
</tr>
<tr>
<td>
DDVPFX_VBICONVERT

</td>
<td>
Data within the vertical blanking interval can be converted independent of the remaining video data.

</td>
</tr>
<tr>
<td>
DDVPFX_VBINOSCALE

</td>
<td>
Scaling can be disabled for data within the vertical blanking interval.

</td>
</tr>
</table>

### -field dwNumAutoFlipSurfaces

Specifies the maximum number of surfaces supported in the autoflip chain, if the hardware video port supports autoflipping. If the hardware video port does not support autoflipping, the driver should set this member to zero.

### -field dwAlignVideoPortBoundary

Specifies the byte alignment restriction, in bytes, of where the hardware video port can be oriented relative to the origin of the surface in the x direction.

### -field dwAlignVideoPortPrescaleWidth

Specifies the byte alignment restriction, in bytes, of how wide the hardware video port data can be when prescaling is performed.

### -field dwAlignVideoPortCropBoundary

Specifies the byte alignment restriction, in bytes, for the left cropping coordinate.

### -field dwAlignVideoPortCropWidth

Specifies the byte alignment restriction, in bytes, for the width of the cropping rectangle.

### -field dwPreshrinkXStep

Indicates that the hardware video port can shrink the video data width in steps of 1/<b>dwPreshrinkXStep</b>. This member is valid only when the DDVPFX_PRESHRINKXS capability is specified.

### -field dwPreshrinkYStep

Indicates that the hardware video port can shrink the video data height in steps of 1/<b>dwPreshrinkYStep</b>. This member is valid only when the DDVPFX_PRESHRINKYS capability is specified.

### -field dwNumVBIAutoFlipSurfaces

Specifies the maximum number of surfaces supported in the autoflip chain, if the hardware video port supports autoflipping. If the hardware video port does not support autoflipping, the driver should set this member to zero. This member works the same way as <b>dwNumAutoFlipSurfaces</b> except that it pertains only to devices that can send the VBI data to a different surface than that to which the normal video is being written.

### -field dwNumPreferredAutoflip

Specifies the optimal number of autoflippable surfaces supported by the hardware.

### -field wNumFilterTapsX

Indicates the number of taps the prescaler uses in the x direction. A value of 0 indicates no prescale, a value of 1 indicates replication, and so on.

### -field wNumFilterTapsY

Indicates the number of taps the prescaler uses in the y direction. A value of 0 indicates no prescale, a value of 1 indicates replication, and so on.

## -remarks

The driver reports the capabilities described by the DDVIDEOPORTCAPS structure when its <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> function is called with the GUID_VideoPortCaps GUID.

## -see-also

<a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>