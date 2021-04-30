---
UID: NF:mfobjects.IMFDXGIDeviceManager.GetVideoService
title: IMFDXGIDeviceManager::GetVideoService (mfobjects.h)
description: Queries the Microsoft Direct3D device for an interface.
helpviewer_keywords: ["GetVideoService","GetVideoService method [Media Foundation]","GetVideoService method [Media Foundation]","IMFDXGIDeviceManager interface","IMFDXGIDeviceManager interface [Media Foundation]","GetVideoService method","IMFDXGIDeviceManager.GetVideoService","IMFDXGIDeviceManager::GetVideoService","mf.imfdxgidevicemanager_getvideoservice","mfobjects/IMFDXGIDeviceManager::GetVideoService"]
old-location: mf\imfdxgidevicemanager_getvideoservice.htm
tech.root: mf
ms.assetid: B0C7C31B-39AF-48B6-8D86-F4DFCC546CDE
ms.date: 12/05/2018
ms.keywords: GetVideoService, GetVideoService method [Media Foundation], GetVideoService method [Media Foundation],IMFDXGIDeviceManager interface, IMFDXGIDeviceManager interface [Media Foundation],GetVideoService method, IMFDXGIDeviceManager.GetVideoService, IMFDXGIDeviceManager::GetVideoService, mf.imfdxgidevicemanager_getvideoservice, mfobjects/IMFDXGIDeviceManager::GetVideoService
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFDXGIDeviceManager::GetVideoService
 - mfobjects/IMFDXGIDeviceManager::GetVideoService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFDXGIDeviceManager.GetVideoService
---

# IMFDXGIDeviceManager::GetVideoService


## -description

Queries the Microsoft Direct3D device for an interface.

## -parameters

### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle">IMFDXGIDeviceManager::OpenDeviceHandle</a>.

### -param riid [in]

The interface identifier (IID) of the requested interface. The Direct3D device supports the following interfaces:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>. To get a pointer to the Direct3D11 device, use <b>IID_ID3D11Device</b> as the <i>riid</i>.</li>
<li>
<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>. To get a pointer to the Direct3D11 video device, use <b>IID_ID3D11VideoDevice</b> as the <i>riid</i>.</li>
</ul>

### -param ppService [out]

Receives a pointer to the requested interface. The caller must release the interface.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

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
<dt><b>MF_E_DXGI_DEVICE_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The DXGI Device Manager was not initialized. The owner of the device must call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_DXGI_NEW_VIDEO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device handle is invalid. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
If a  <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>  is specified and the D3D device created is using the reference rasterizer or WARP.  Or it is a hardware device and you are using the Microsoft Basic Display Adapter.

</td>
</tr>
</table>

## -remarks

If the method returns <b>MF_E_DXGI_NEW_VIDEO_DEVICE</b>, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle">IMFDXGIDeviceManager::CloseDeviceHandle</a> to close the handle and then call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle">OpenDeviceHandle</a> again to get a new handle. The  <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a> method invalidates all open device handles.

For more info see, <a href="/windows/desktop/medfound/supporting-direct3d-11-video-decoding-in-media-foundation">Supporting Direct3D 11 Video Decoding in Media Foundation</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>