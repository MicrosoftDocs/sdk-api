---
UID: NF:dxva2api.IDirect3DDeviceManager9.CloseDeviceHandle
title: IDirect3DDeviceManager9::CloseDeviceHandle (dxva2api.h)
description: Closes a Direct3D device handle.
helpviewer_keywords: ["5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a","CloseDeviceHandle","CloseDeviceHandle method [Media Foundation]","CloseDeviceHandle method [Media Foundation]","IDirect3DDeviceManager9 interface","IDirect3DDeviceManager9 interface [Media Foundation]","CloseDeviceHandle method","IDirect3DDeviceManager9.CloseDeviceHandle","IDirect3DDeviceManager9::CloseDeviceHandle","dxva2api/IDirect3DDeviceManager9::CloseDeviceHandle","mf.idirect3ddevicemanager9_closedevicehandle"]
old-location: mf\idirect3ddevicemanager9_closedevicehandle.htm
tech.root: mf
ms.assetid: 5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a
ms.date: 12/05/2018
ms.keywords: 5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a, CloseDeviceHandle, CloseDeviceHandle method [Media Foundation], CloseDeviceHandle method [Media Foundation],IDirect3DDeviceManager9 interface, IDirect3DDeviceManager9 interface [Media Foundation],CloseDeviceHandle method, IDirect3DDeviceManager9.CloseDeviceHandle, IDirect3DDeviceManager9::CloseDeviceHandle, dxva2api/IDirect3DDeviceManager9::CloseDeviceHandle, mf.idirect3ddevicemanager9_closedevicehandle
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
 - IDirect3DDeviceManager9::CloseDeviceHandle
 - dxva2api/IDirect3DDeviceManager9::CloseDeviceHandle
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
 - IDirect3DDeviceManager9.CloseDeviceHandle
---

# IDirect3DDeviceManager9::CloseDeviceHandle


## -description

Closes a Direct3D device handle. Call this method to release a device handle retrieved by the <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">IDirect3DDeviceManager9::OpenDeviceHandle</a> method.

## -parameters

### -param hDevice [in]

Handle to the Direct3D device.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>