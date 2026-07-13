---
UID: NS:ddraw._DDCOLORCONTROL
title: DDCOLORCONTROL
description: The DDCOLORCONTROL structure defines the color controls associated with a Microsoft DirectDraw [*video port extensions (VPE)*](/windows-hardware/drivers/display/video-port-extensions-to-directx) object.
tech.root: directdraw
ms.date: 07/11/2022
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ddraw.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DDCOLORCONTROL, *LPDDCOLORCONTROL
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ddraw.h
api_name:
 - _DDCOLORCONTROL
 - LPDDCOLORCONTROL
 - DDCOLORCONTROL
f1_keywords:
 - _DDCOLORCONTROL
 - ddraw/_DDCOLORCONTROL
 - LPDDCOLORCONTROL
 - ddraw/LPDDCOLORCONTROL
 - DDCOLORCONTROL
 - ddraw/DDCOLORCONTROL
dev_langs:
 - c++
helpviewer_keywords:
 - _DDCOLORCONTROL
---

## -description

The DDCOLORCONTROL structure defines the color controls associated with a Microsoft DirectDraw [*video port extensions (VPE)*](/windows-hardware/drivers/display/video-port-extensions-to-directx) object.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DDCOLORCONTROL structure.

### -field dwFlags

Indicates a set of flags that specify what structure members contain valid data. When the structure is returned by [*DdVideoPortColorControl*](https://msdn.microsoft.com/library/ff550383\(v=vs.85\)), it also indicates what options are supported by the VPE object. This member can be a bitwise OR of the values listed in the following table.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDCOLOR_BRIGHTNESS</p></td>
<td><p>The <strong>lBrightness</strong> member contains valid data.</p></td>
</tr>
<tr class="even">
<td><p>DDCOLOR_CONTRAST</p></td>
<td><p>The <strong>lContrast</strong> member contains valid data.</p></td>
</tr>
<tr class="odd">
<td><p>DDCOLOR_COLORENABLE</p></td>
<td><p>The <strong>lColorEnable</strong> member contains valid data.</p></td>
</tr>
<tr class="even">
<td><p>DDCOLOR_GAMMA</p></td>
<td><p>The <strong>lGamma</strong> member contains valid data.</p></td>
</tr>
<tr class="odd">
<td><p>DDCOLOR_HUE</p></td>
<td><p>The <strong>lHue</strong> member contains valid data.</p></td>
</tr>
<tr class="even">
<td><p>DDCOLOR_SATURATION</p></td>
<td><p>The <strong>lSaturation</strong> member contains valid data.</p></td>
</tr>
<tr class="odd">
<td><p>DDCOLOR_SHARPNESS</p></td>
<td><p>The <strong>lSharpness</strong> member contains valid data.</p></td>
</tr>
</tbody>
</table>

### -field lBrightness

Specifies the luminance intensity (Black Level), in IRE units\*100. This member can range from 0 to 10,000, with a default value of 750 (7.5 IRE).

### -field lContrast

Specifies the relative difference between higher and lower intensity luminance values, in IRE units\*100. This member can range from 0 to 20,000, with a default value of 10,000 (100 IRE). Higher values of contrast cause darker luminance values to tend toward black, and cause lighter luminance values to tend toward white. Lower values of contrast cause all luminance values to move toward the middle luminance values.

### -field lHue

Specifies the phase relationship of the chrominance components. Hue is specified in degrees, with a valid range of -180 to 180. The default is 0 degrees.

### -field lSaturation

Specifies the color intensity, in IRE units\*100. This member can range from 0 to 20,000, with a default value of 10,000 (100 IRE).

### -field lSharpness

Specifies the sharpness in arbitrary units. The valid range is 0 to 10, with a default value of 5.

### -field lGamma

Controls the amount of gamma correction applied to the luminance values. The valid range is 1 to 500 gamma units, with a default of 1.

### -field lColorEnable

Specifies a flag indicating whether color is used. If this member is zero, color is not used; if it is 1, then color is used. The default value is 1.

### -field dwReserved1

Reserved for system use, and should be ignored.

## -remarks

## -see-also

* [DdVideoPortColorControl](/windows/win32/api/ddrawint/nc-ddrawint-pdd_vportcb_colorcontrol)
