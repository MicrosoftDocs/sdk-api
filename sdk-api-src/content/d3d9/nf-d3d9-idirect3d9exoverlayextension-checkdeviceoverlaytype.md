---
UID: NF:d3d9.IDirect3D9ExOverlayExtension.CheckDeviceOverlayType
title: IDirect3D9ExOverlayExtension::CheckDeviceOverlayType (d3d9.h)
description: Queries the overlay hardware capabilities of a Direct3D device. (IDirect3D9ExOverlayExtension.CheckDeviceOverlayType)
helpviewer_keywords: ["CheckDeviceOverlayType","CheckDeviceOverlayType method [Media Foundation]","CheckDeviceOverlayType method [Media Foundation]","IDirect3D9ExOverlayExtension interface","IDirect3D9ExOverlayExtension interface [Media Foundation]","CheckDeviceOverlayType method","IDirect3D9ExOverlayExtension.CheckDeviceOverlayType","IDirect3D9ExOverlayExtension::CheckDeviceOverlayType","d3d9/IDirect3D9ExOverlayExtension::CheckDeviceOverlayType","mf.idirect3d9exoverlayextension_checkdeviceoverlaytype"]
old-location: mf\idirect3d9exoverlayextension_checkdeviceoverlaytype.htm
tech.root: mf
ms.assetid: 83880b6f-f8a0-4be4-a400-ea86ca41f9e7
ms.date: 12/05/2018
ms.keywords: CheckDeviceOverlayType, CheckDeviceOverlayType method [Media Foundation], CheckDeviceOverlayType method [Media Foundation],IDirect3D9ExOverlayExtension interface, IDirect3D9ExOverlayExtension interface [Media Foundation],CheckDeviceOverlayType method, IDirect3D9ExOverlayExtension.CheckDeviceOverlayType, IDirect3D9ExOverlayExtension::CheckDeviceOverlayType, d3d9/IDirect3D9ExOverlayExtension::CheckDeviceOverlayType, mf.idirect3d9exoverlayextension_checkdeviceoverlaytype
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9ExOverlayExtension::CheckDeviceOverlayType
 - d3d9/IDirect3D9ExOverlayExtension::CheckDeviceOverlayType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3D9ExOverlayExtension.CheckDeviceOverlayType
---

# IDirect3D9ExOverlayExtension::CheckDeviceOverlayType


## -description

Queries the overlay hardware capabilities of a Direct3D device.

## -parameters

### -param Adapter [in]

An ordinal number that denotes the display adapter. <b>D3DADAPTER_DEFAULT</b> is always the primary display adapter.

### -param DevType [in]

Specifies the Direct3D device type as a member of the <b>D3DDEVTYPE</b> enumerated type.

### -param OverlayWidth [in]

The width of the overlay to create, in pixels.

### -param OverlayHeight [in]

The height of the overlay to create, in pixels.

### -param OverlayFormat [in]

The surface format of the overlay.

### -param pDisplayMode [in]

A pointer to a <b>D3DDISPLAYMODEEX</b> structure that specifies the display mode that will be used. If this parameter is <b>NULL</b>, the current display mode is assumed.

### -param DisplayRotation [in]

Specifies the display rotation mode as a member of the <b>D3DDISPLAYROTATION</b> enumerated type.

### -param pOverlayCaps [out]

A pointer to a <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps">D3DOVERLAYCAPS</a> structure. If the driver supports the overlay settings specified in the input parameters, the method fills this structure with the capabilities of the overlay hardware.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter, or the device does not support hardware overlay.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_UNSUPPORTEDOVERLAY</b></dt>
</dl>
</td>
<td width="60%">
The device does not support overlay for the specified size or display mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_UNSUPPORTEDOVERLAYFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The device does not support overlay for the specified surface format.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/hardware-overlay-support">Hardware Overlay Support</a>



<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension">IDirect3D9ExOverlayExtension</a>
