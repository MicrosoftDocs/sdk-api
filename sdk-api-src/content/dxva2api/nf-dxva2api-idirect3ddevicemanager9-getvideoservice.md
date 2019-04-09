---
UID: NF:dxva2api.IDirect3DDeviceManager9.GetVideoService
title: IDirect3DDeviceManager9::GetVideoService (dxva2api.h)
author: windows-sdk-content
description: Gets a DirectX Video Acceleration (DXVA) service interface.
old-location: mf\idirect3ddevicemanager9_getvideoservice.htm
tech.root: medfound
ms.assetid: 2e62a750-3017-4dd7-9fbc-e2c641f6cf10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2e62a750-3017-4dd7-9fbc-e2c641f6cf10, GetVideoService, GetVideoService method [Media Foundation], GetVideoService method [Media Foundation],IDirect3DDeviceManager9 interface, IDirect3DDeviceManager9 interface [Media Foundation],GetVideoService method, IDirect3DDeviceManager9.GetVideoService, IDirect3DDeviceManager9::GetVideoService, dxva2api/IDirect3DDeviceManager9::GetVideoService, mf.idirect3ddevicemanager9_getvideoservice
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirect3DDeviceManager9.GetVideoService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDeviceManager9::GetVideoService


## -description


Gets a DirectX Video Acceleration (DXVA) service interface.
        


## -parameters




### -param hDevice [in]

A handle to a Direct3D device. To get a device handle, call <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">IDirect3DDeviceManager9::OpenDeviceHandle</a>.
          


### -param riid [in]

The interface identifier (IID) of the requested interface. The Direct3D device might support the following DXVA service interfaces:
          

<ul>
<li>
<a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fa33a9e9-4e91-4eb7-91c2-5b0c63ab7688">IDirectXVideoProcessorService</a>
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
The Direct3D device manager was not initialized. The owner of the device must call <a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">IDirect3DDeviceManager9::ResetDevice</a>.
              

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



If the method returns <b>DXVA2_E_NEW_VIDEO_DEVICE</b>, call <a href="https://msdn.microsoft.com/5c074823-d1f4-4db1-87ab-bbdb6d0a7a5a">IDirect3DDeviceManager9::CloseDeviceHandle</a> to close the handle and then call <a href="https://msdn.microsoft.com/74cd2260-279a-4956-8fce-40f8008b6797">OpenDeviceHandle</a> again to get a new handle. The <a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">IDirect3DDeviceManager9::ResetDevice</a> method invalidates all open device handles.


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




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a>
 

 

