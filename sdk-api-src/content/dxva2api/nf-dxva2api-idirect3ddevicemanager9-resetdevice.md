---
UID: NF:dxva2api.IDirect3DDeviceManager9.ResetDevice
title: IDirect3DDeviceManager9::ResetDevice (dxva2api.h)
description: Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.
helpviewer_keywords: ["01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33","IDirect3DDeviceManager9 interface [Media Foundation]","ResetDevice method","IDirect3DDeviceManager9.ResetDevice","IDirect3DDeviceManager9::ResetDevice","ResetDevice","ResetDevice method [Media Foundation]","ResetDevice method [Media Foundation]","IDirect3DDeviceManager9 interface","dxva2api/IDirect3DDeviceManager9::ResetDevice","mf.idirect3ddevicemanager9_resetdevice"]
old-location: mf\idirect3ddevicemanager9_resetdevice.htm
tech.root: mf
ms.assetid: 01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33
ms.date: 12/05/2018
ms.keywords: 01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33, IDirect3DDeviceManager9 interface [Media Foundation],ResetDevice method, IDirect3DDeviceManager9.ResetDevice, IDirect3DDeviceManager9::ResetDevice, ResetDevice, ResetDevice method [Media Foundation], ResetDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::ResetDevice, mf.idirect3ddevicemanager9_resetdevice
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDirect3DDeviceManager9::ResetDevice
 - dxva2api/IDirect3DDeviceManager9::ResetDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirect3DDeviceManager9.ResetDevice
---

# IDirect3DDeviceManager9::ResetDevice


## -description

Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.

## -parameters

### -param pDevice [in]

Pointer to the <b>IDirect3DDevice9</b> interface of the Direct3D device.

### -param resetToken [in]

Token received in the <i>pResetToken</i> parameter of the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9">DXVA2CreateDirect3DDeviceManager9</a> function.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid token

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
Direct3D device error.

</td>
</tr>
</table>

## -remarks

When you first create the Direct3D device manager, call this method with a pointer to the Direct3D device. The device manager does not create the device; the caller must provide the device pointer initially.

Also call this method if the Direct3D device becomes lost and you need to reset the device or create a new device. This occurs if <b>IDirect3DDevice9::TestCooperativeLevel</b> returns D3DERR_DEVICELOST or D3DERR_DEVICENOTRESET. For more information about lost devices, see the Direct3D documentation.

The <i>resetToken</i> parameter ensures that only the component which originally created the device manager can invalidate the current device.

If this method succeeds, all open device handles become invalid.

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>