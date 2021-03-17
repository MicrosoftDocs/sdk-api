---
UID: NF:dxva2api.IDirect3DDeviceManager9.UnlockDevice
title: IDirect3DDeviceManager9::UnlockDevice (dxva2api.h)
description: Unlocks the Direct3D device.
helpviewer_keywords: ["IDirect3DDeviceManager9 interface [Media Foundation]","UnlockDevice method","IDirect3DDeviceManager9.UnlockDevice","IDirect3DDeviceManager9::UnlockDevice","UnlockDevice","UnlockDevice method [Media Foundation]","UnlockDevice method [Media Foundation]","IDirect3DDeviceManager9 interface","dxva2api/IDirect3DDeviceManager9::UnlockDevice","e5be74bc-55a2-4c8a-86eb-97b96a4091e7","mf.idirect3ddevicemanager9_unlockdevice"]
old-location: mf\idirect3ddevicemanager9_unlockdevice.htm
tech.root: mf
ms.assetid: e5be74bc-55a2-4c8a-86eb-97b96a4091e7
ms.date: 12/05/2018
ms.keywords: IDirect3DDeviceManager9 interface [Media Foundation],UnlockDevice method, IDirect3DDeviceManager9.UnlockDevice, IDirect3DDeviceManager9::UnlockDevice, UnlockDevice, UnlockDevice method [Media Foundation], UnlockDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::UnlockDevice, e5be74bc-55a2-4c8a-86eb-97b96a4091e7, mf.idirect3ddevicemanager9_unlockdevice
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
 - IDirect3DDeviceManager9::UnlockDevice
 - dxva2api/IDirect3DDeviceManager9::UnlockDevice
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
 - IDirect3DDeviceManager9.UnlockDevice
---

# IDirect3DDeviceManager9::UnlockDevice


## -description

Unlocks the Direct3D device. Call this method to release the device after calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice">IDirect3DDeviceManager9::LockDevice</a>.

## -parameters

### -param hDevice [in]

Handle to the Direct3D device. To get the device handle, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">IDirect3DDeviceManager9::OpenDeviceHandle</a>.

### -param fSaveState [in]

If <b>TRUE</b>, the method saves the Direct3D device state in a state block. Internally, the method uses the Direct3D <b>IDirect3DStateBlock9</b> interface to save the device state. The next time you call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice">LockDevice</a> with the same device handle, the state block is restored.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The specified device handle is not locked, or is not a valid handle.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>