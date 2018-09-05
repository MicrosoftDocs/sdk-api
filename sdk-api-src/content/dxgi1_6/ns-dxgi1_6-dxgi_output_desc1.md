---
UID: NS:dxgi1_6.DXGI_OUTPUT_DESC1
title: DXGI_OUTPUT_DESC1
author: windows-sdk-content
description: Describes an output or physical connection between the adapter (video card) and a device, including additional information about color capabilities and connection type.
old-location: direct3ddxgi\dxgi_output_desc1.htm
old-project: direct3ddxgi
ms.assetid: 5215EF2C-9511-4B21-B574-3447FA5896F7
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: DXGI_OUTPUT_DESC1, DXGI_OUTPUT_DESC1 structure [DXGI], direct3ddxgi.dxgi_output_desc1, dxgi1_6/DXGI_OUTPUT_DESC1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_6.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_OUTPUT_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_6.h
api_name:
 - DXGI_OUTPUT_DESC1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_OUTPUT_DESC1 structure


## -description


Describes an output or physical connection between the adapter (video card) and a device, including additional information about color capabilities and connection type.


## -struct-fields




### -field DeviceName

Type: <b>WCHAR[32]</b>

A string that contains the name of the output device.


### -field DesktopCoordinates

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure containing the bounds of the output in desktop coordinates. Desktop coordinates depend on the dots per inch (DPI) of the desktop.
	  For info about writing DPI-aware Win32 apps, see <a href="https://msdn.microsoft.com/784e308d-904b-40ac-bf98-1a00fa1c9cf0">High DPI</a>.


### -field AttachedToDesktop

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True if the output is attached to the desktop; otherwise, false.


### -field Rotation

Type: <b><a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a></b>

A member of the <a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a> enumerated type describing on how an image is rotated by the output.


### -field Monitor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMONITOR</a></b>

An <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMONITOR</a> handle that represents the display monitor. For more information, see <a href="https://msdn.microsoft.com/c43c1401-52d3-485e-a418-205df5737040">HMONITOR and the Device Context</a>.


### -field BitsPerColor

Type: <b>UINT</b>

The number of bits per color channel for the active wire format of the display attached to this output.


### -field ColorSpace

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

The current advanced color capabilities of the display attached to this output. Specifically, whether its capable of reproducing color and luminance values outside of the sRGB color space.
	    A value of DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709 indicates that the display is limited to SDR/sRGB; A value of DXGI_COLOR_SPACE_RGB_FULL_G2048_NONE_P2020 indicates that the display supports
	    advanced color capabilities.

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

Type: <b>FLAOT</b>

The maximum luminance, in nits, that the display attached to this output is capable of rendering; unlike MaxLuminance, this value is valid for a color that fills the entire area of the
	  panel. Content should not exceed this value across the entire panel for optimal rendering. This value will usually come from the EDID of the corresponding display or sometimes from an
	  override.


#### - InternalOutput

Type: <b>BOOL</b>

True if this output is attached to an internal/integrated display panel; otherwise, false.


## -remarks



The <b>DXGI_OUTPUT_DESC1</b> structure is initialized by the <a href="https://msdn.microsoft.com/DE251D64-BB41-49D7-AC46-791089502286">IDXGIOutput6::GetDesc1</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

