---
UID: NF:dxva2api.IDirect3DDeviceManager9.GetVideoService
title: IDirect3DDeviceManager9::GetVideoService (dxva2api.h)
description: Gets a DirectX Video Acceleration (DXVA) service interface.
helpviewer_keywords: ["2e62a750-3017-4dd7-9fbc-e2c641f6cf10","GetVideoService","GetVideoService method [Media Foundation]","GetVideoService method [Media Foundation]","IDirect3DDeviceManager9 interface","IDirect3DDeviceManager9 interface [Media Foundation]","GetVideoService method","IDirect3DDeviceManager9.GetVideoService","IDirect3DDeviceManager9::GetVideoService","dxva2api/IDirect3DDeviceManager9::GetVideoService","mf.idirect3ddevicemanager9_getvideoservice"]
old-location: mf\idirect3ddevicemanager9_getvideoservice.htm
tech.root: mf
ms.assetid: 2e62a750-3017-4dd7-9fbc-e2c641f6cf10
ms.date: 12/05/2018
ms.keywords: 2e62a750-3017-4dd7-9fbc-e2c641f6cf10, GetVideoService, GetVideoService method [Media Foundation], GetVideoService method [Media Foundation],IDirect3DDeviceManager9 interface, IDirect3DDeviceManager9 interface [Media Foundation],GetVideoService method, IDirect3DDeviceManager9.GetVideoService, IDirect3DDeviceManager9::GetVideoService, dxva2api/IDirect3DDeviceManager9::GetVideoService, mf.idirect3ddevicemanager9_getvideoservice
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
 - IDirect3DDeviceManager9::GetVideoService
 - dxva2api/IDirect3DDeviceManager9::GetVideoService
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
 - IDirect3DDeviceManager9.GetVideoService
---

# IDirect3DDeviceManager9::GetVideoService


## -description

Gets a DirectX Video Acceleration (DXVA) service interface.

## -parameters

### -param hDevice [in]

A handle to a Direct3D device. To get a device handle, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">IDirect3DDeviceManager9::OpenDeviceHandle</a>.

### -param riid [in]

The interface identifier (IID) of the requested interface. The Direct3D device might support the following DXVA service interfaces:
          

<ul>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>
</li>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>
</li>
</ul>

### -param ppService [out]

Receives a pointer to the requested interface. The caller must release the interface.

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
<dt><b>DXVA2_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The Direct3D device does not support video acceleration.
              

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is not a Direct3D device handle.
              

</td>
</tr>
</table>

## -remarks

If the method returns <b>DXVA2_E_NEW_VIDEO_DEVICE</b>, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle">IDirect3DDeviceManager9::CloseDeviceHandle</a> to close the handle and then call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">OpenDeviceHandle</a> again to get a new handle. The <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a> method invalidates all open device handles.


#### Examples


```cpp
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a>