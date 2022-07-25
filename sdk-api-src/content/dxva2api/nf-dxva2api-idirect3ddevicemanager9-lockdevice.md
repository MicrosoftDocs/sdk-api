---
UID: NF:dxva2api.IDirect3DDeviceManager9.LockDevice
title: IDirect3DDeviceManager9::LockDevice (dxva2api.h)
description: Gives the caller exclusive access to the Direct3D device.
helpviewer_keywords: ["51631747-04af-448e-97cf-25a329d4fbb4","IDirect3DDeviceManager9 interface [Media Foundation]","LockDevice method","IDirect3DDeviceManager9.LockDevice","IDirect3DDeviceManager9::LockDevice","LockDevice","LockDevice method [Media Foundation]","LockDevice method [Media Foundation]","IDirect3DDeviceManager9 interface","dxva2api/IDirect3DDeviceManager9::LockDevice","mf.idirect3ddevicemanager9_lockdevice"]
old-location: mf\idirect3ddevicemanager9_lockdevice.htm
tech.root: mf
ms.assetid: 51631747-04af-448e-97cf-25a329d4fbb4
ms.date: 12/05/2018
ms.keywords: 51631747-04af-448e-97cf-25a329d4fbb4, IDirect3DDeviceManager9 interface [Media Foundation],LockDevice method, IDirect3DDeviceManager9.LockDevice, IDirect3DDeviceManager9::LockDevice, LockDevice, LockDevice method [Media Foundation], LockDevice method [Media Foundation],IDirect3DDeviceManager9 interface, dxva2api/IDirect3DDeviceManager9::LockDevice, mf.idirect3ddevicemanager9_lockdevice
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
 - IDirect3DDeviceManager9::LockDevice
 - dxva2api/IDirect3DDeviceManager9::LockDevice
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
 - IDirect3DDeviceManager9.LockDevice
---

# IDirect3DDeviceManager9::LockDevice


## -description

Gives the caller exclusive access to the Direct3D device.

## -parameters

### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">IDirect3DDeviceManager9::OpenDeviceHandle</a>.

### -param ppDevice [out]

Receives a pointer to the device's <b>IDirect3DDevice9</b> interface.

### -param fBlock [in]

Specifies whether to wait for the device lock. If the device is already locked and this parameter is <b>TRUE</b>, the method blocks until the device is unlocked. Otherwise, if the device is locked and this parameter is <b>FALSE</b>, the method returns immediately with the error code <b>DXVA2_E_VIDEO_DEVICE_LOCKED</b>.

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
<dt><b>DXVA2_E_NEW_VIDEO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device handle is invalid.
              

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
<tr>
<td width="40%">
<dl>
<dt><b>DXVA2_E_VIDEO_DEVICE_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The device is locked and <i>fBlock</i> is <b>FALSE</b>.
              

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
</table>

## -remarks

When you are done using the Direct3D device, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice">IDirect3DDeviceManager9::UnlockDevice</a> to unlock to the device.
      

If the method returns <b>DXVA2_E_NEW_VIDEO_DEVICE</b>, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle">IDirect3DDeviceManager9::CloseDeviceHandle</a> to close the handle and then call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">OpenDeviceHandle</a> again to get a new handle. The <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a> method invalidates all open device handles.
      

If <i>fBlock</i> is <b>TRUE</b>, this method can potentially deadlock. For example, it will deadlock if a thread calls <b>LockDevice</b> and then waits on another thread that calls <b>LockDevice</b>. It will also deadlock if a thread calls <b>LockDevice</b> twice without calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice">UnlockDevice</a> in between.
      


#### Examples


```cpp
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>