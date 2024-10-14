---
UID: NS:dxgi1_6.DXGI_OUTPUT_DESC1
title: DXGI_OUTPUT_DESC1 (dxgi1_6.h)
description: Describes an output or physical connection between the adapter (video card) and a device, including additional information about color capabilities and connection type.
helpviewer_keywords: ["DXGI_OUTPUT_DESC1","DXGI_OUTPUT_DESC1 structure [DXGI]","direct3ddxgi.dxgi_output_desc1","dxgi1_6/DXGI_OUTPUT_DESC1"]
old-location: direct3ddxgi\dxgi_output_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 5215EF2C-9511-4B21-B574-3447FA5896F7
ms.date: 12/05/2018
ms.keywords: DXGI_OUTPUT_DESC1, DXGI_OUTPUT_DESC1 structure [DXGI], direct3ddxgi.dxgi_output_desc1, dxgi1_6/DXGI_OUTPUT_DESC1
req.header: dxgi1_6.h
req.include-header: 
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
req.typenames: DXGI_OUTPUT_DESC1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTPUT_DESC1
 - dxgi1_6/DXGI_OUTPUT_DESC1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_6.h
api_name:
 - DXGI_OUTPUT_DESC1
---

## -description

Describes an output or physical connection between the adapter (video card) and a device, including additional information about color capabilities and connection type.

## -struct-fields

### -field DeviceName

Type: <b>WCHAR[32]</b>

A string that contains the name of the output device.

### -field DesktopCoordinates

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the bounds of the output in desktop coordinates. Desktop coordinates depend on the dots per inch (DPI) of the desktop.
	  For info about writing DPI-aware Win32 apps, see <a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a>.

### -field AttachedToDesktop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

True if the output is attached to the desktop; otherwise, false.

### -field Rotation

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION</a></b>

A member of the <a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION</a> enumerated type describing on how an image is rotated by the output.

### -field Monitor

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMONITOR</a></b>

An <a href="/windows/desktop/WinProg/windows-data-types">HMONITOR</a> handle that represents the display monitor. For more information, see <a href="/windows/desktop/gdi/hmonitor-and-the-device-context">HMONITOR and the Device Context</a>.

### -field BitsPerColor

Type: <b>UINT</b>

The number of bits per color channel for the active wire format of the display attached to this output.

### -field ColorSpace

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

The current advanced color capabilities of the display attached to this output. Specifically, whether it's capable of reproducing color and luminance values outside of the sRGB color space. A value of **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709** indicates that the display is limited to SDR/sRGB. A value of **DXGI_COLOR_SPACE_RGB_FULL_G2048_NONE_P2020** indicates that the display supports advanced color capabilities. **DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709** is currently not a color space that displays use; it's simply an intermediary swap-chain color space.

For detailed luminance and color capabilities, see additional members of this struct.

### -field RedPrimary

Type: <b>FLOAT[2]</b>

The red color primary, in xy coordinates, of the display attached to this output. This value will usually come from the EDID of the corresponding display or sometimes from an override.

### -field GreenPrimary

Type: <b>FLOAT[2]</b>

The green color primary, in xy coordinates, of the display attached to this output. This value will usually come from the EDID of the corresponding display or sometimes from an override.

### -field BluePrimary

Type: <b>FLOAT[2]</b>

The blue color primary, in xy coordinates, of the display attached to this output. This value will usually come from the EDID of the corresponding display or sometimes from an override.

### -field WhitePoint

Type: <b>FLOAT[2]</b>

The white point, in xy coordinates, of the display attached to this output. This value will usually come from the EDID of the corresponding display or sometimes from an override.

### -field MinLuminance

Type: <b>FLOAT</b>

The minimum luminance, in nits, that the display attached to this output is capable of rendering. Content should not exceed this minimum value for optimal rendering. This value will
	  usually come from the EDID of the corresponding display or sometimes from an override.

### -field MaxLuminance

Type: <b>FLOAT</b>

The maximum luminance, in nits, that the display attached to this output is capable of rendering; this value is likely only valid for a small area of the panel. Content should not exceed
	  this minimum value for optimal rendering. This value will usually come from the EDID of the corresponding display or sometimes from an override.

### -field MaxFullFrameLuminance

Type: <b>FLOAT</b>

The maximum luminance, in nits, that the display attached to this output is capable of rendering; unlike MaxLuminance, this value is valid for a color that fills the entire area of the
	  panel. Content should not exceed this value across the entire panel for optimal rendering. This value will usually come from the EDID of the corresponding display or sometimes from an
	  override.

## -remarks

The <b>DXGI_OUTPUT_DESC1</b> structure is initialized by the <a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1">IDXGIOutput6::GetDesc1</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
