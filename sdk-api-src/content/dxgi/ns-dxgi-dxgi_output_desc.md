---
UID: NS:dxgi.DXGI_OUTPUT_DESC
title: DXGI_OUTPUT_DESC (dxgi.h)
description: Describes an output or physical connection between the adapter (video card) and a device.
helpviewer_keywords: ["DXGI_OUTPUT_DESC","DXGI_OUTPUT_DESC structure [DXGI]","d70793ef-13c9-f3fa-6590-c3b793e1191b","direct3ddxgi.dxgi_output_desc","dxgi/DXGI_OUTPUT_DESC"]
old-location: direct3ddxgi\dxgi_output_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_output_desc.htm
ms.date: 12/05/2018
ms.keywords: DXGI_OUTPUT_DESC, DXGI_OUTPUT_DESC structure [DXGI], d70793ef-13c9-f3fa-6590-c3b793e1191b, direct3ddxgi.dxgi_output_desc, dxgi/DXGI_OUTPUT_DESC
req.header: dxgi.h
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
req.typenames: DXGI_OUTPUT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_OUTPUT_DESC
 - dxgi/DXGI_OUTPUT_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_OUTPUT_DESC
---

# DXGI_OUTPUT_DESC structure


## -description

Describes an output or physical connection between the adapter (video card) and a device.

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

## -remarks

The <b>DXGI_OUTPUT_DESC</b> structure is initialized by the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdesc">IDXGIOutput::GetDesc</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>