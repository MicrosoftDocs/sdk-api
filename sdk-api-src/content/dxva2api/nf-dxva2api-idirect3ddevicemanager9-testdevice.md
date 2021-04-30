---
UID: NF:dxva2api.IDirect3DDeviceManager9.TestDevice
title: IDirect3DDeviceManager9::TestDevice (dxva2api.h)
description: Tests whether a Direct3D device handle is valid.
helpviewer_keywords: ["IDirect3DDeviceManager9 interface [Media Foundation]","TestDevice method","IDirect3DDeviceManager9.TestDevice","IDirect3DDeviceManager9::TestDevice","TestDevice","TestDevice method [Media Foundation]","TestDevice method [Media Foundation]","IDirect3DDeviceManager9 interface","dxva2api/IDirect3DDeviceManager9::TestDevice","e97acc5d-1b6a-43ae-a057-9c650d7126ab","mf.idirect3ddevicemanager9_testdevice"]
old-location: mf\idirect3ddevicemanager9_testdevice.htm
tech.root: mf
ms.assetid: e97acc5d-1b6a-43ae-a057-9c650d7126ab
ms.date: 12/05/2018
ms.keywords: IDirect3DDeviceManager9 interface [Media Foundation],TestDevice method, IDirect3DDeviceManager9.TestDevice, IDirect3DDeviceManager9::TestDevice, TestDevice, TestDevice method [Media Foundation], TestDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::TestDevice, e97acc5d-1b6a-43ae-a057-9c650d7126ab, mf.idirect3ddevicemanager9_testdevice
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
 - IDirect3DDeviceManager9::TestDevice
 - dxva2api/IDirect3DDeviceManager9::TestDevice
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
 - IDirect3DDeviceManager9.TestDevice
---

# IDirect3DDeviceManager9::TestDevice


## -description

Tests whether a Direct3D device handle is valid.

## -parameters

### -param hDevice [in]

Handle to a Direct3D device. To get a device handle, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">IDirect3DDeviceManager9::OpenDeviceHandle</a>.

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
The device handle is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not a Direct3D device handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DXVA2_E_NEW_VIDEO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device handle is invalid.

</td>
</tr>
</table>

## -remarks

If the method returns DXVA2_E_NEW_VIDEO_DEVICE, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle">IDirect3DDeviceManager9::CloseDeviceHandle</a> to close the handle and then call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">OpenDeviceHandle</a> again to get a new handle. The <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a> method invalidates all open device handles.

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>