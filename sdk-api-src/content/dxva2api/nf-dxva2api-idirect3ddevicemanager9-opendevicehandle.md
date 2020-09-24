---
UID: NF:dxva2api.IDirect3DDeviceManager9.OpenDeviceHandle
title: IDirect3DDeviceManager9::OpenDeviceHandle (dxva2api.h)
description: Gets a handle to the Direct3D device.
helpviewer_keywords: ["74cd2260-279a-4956-8fce-40f8008b6797","IDirect3DDeviceManager9 interface [Media Foundation]","OpenDeviceHandle method","IDirect3DDeviceManager9.OpenDeviceHandle","IDirect3DDeviceManager9::OpenDeviceHandle","OpenDeviceHandle","OpenDeviceHandle method [Media Foundation]","OpenDeviceHandle method [Media Foundation]","IDirect3DDeviceManager9 interface","dxva2api/IDirect3DDeviceManager9::OpenDeviceHandle","mf.idirect3ddevicemanager9_opendevicehandle"]
old-location: mf\idirect3ddevicemanager9_opendevicehandle.htm
tech.root: mf
ms.assetid: 74cd2260-279a-4956-8fce-40f8008b6797
ms.date: 12/05/2018
ms.keywords: 74cd2260-279a-4956-8fce-40f8008b6797, IDirect3DDeviceManager9 interface [Media Foundation],OpenDeviceHandle method, IDirect3DDeviceManager9.OpenDeviceHandle, IDirect3DDeviceManager9::OpenDeviceHandle, OpenDeviceHandle, OpenDeviceHandle method [Media Foundation], OpenDeviceHandle method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::OpenDeviceHandle, mf.idirect3ddevicemanager9_opendevicehandle
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
 - IDirect3DDeviceManager9::OpenDeviceHandle
 - dxva2api/IDirect3DDeviceManager9::OpenDeviceHandle
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
 - IDirect3DDeviceManager9.OpenDeviceHandle
---

# IDirect3DDeviceManager9::OpenDeviceHandle


## -description

Gets a handle to the Direct3D device.

## -parameters

### -param phDevice [out]

Receives the device handle.

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
<dt><b>DXVA2_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Direct3D device manager was not initialized. The owner of the device must call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a>.

</td>
</tr>
</table>

## -remarks

To get the Direct3D device's <b>IDirect3DDevice9</b> pointer, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice">IDirect3DDeviceManager9::LockDevice</a> with the handle returned in <i>phDevice</i>. Close the device handle when you are done using it, by calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle">IDirect3DDeviceManager9::CloseDeviceHandle</a>.

To test whether a device handle is still valid, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice">IDirect3DDeviceManager9::TestDevice</a>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>