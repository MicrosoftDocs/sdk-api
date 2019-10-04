---
UID: NN:dxva2api.IDirect3DDeviceManager9
title: IDirect3DDeviceManager9 (dxva2api.h)
author: windows-sdk-content
description: Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.
old-location: mf\idirect3ddevicemanager9.htm
tech.root: medfound
ms.assetid: e661e666-dc51-4a71-9ecd-62a667bb217d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3DDeviceManager9, IDirect3DDeviceManager9 interface [Media Foundation], IDirect3DDeviceManager9 interface [Media Foundation],described, dxva2api/IDirect3DDeviceManager9, e661e666-dc51-4a71-9ecd-62a667bb217d, mf.idirect3ddevicemanager9
ms.topic: interface
f1_keywords: 
 - "dxva2api/IDirect3DDeviceManager9"
dev_langs:
 - c++
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
 - IDirect3DDeviceManager9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDeviceManager9 interface


## -description


Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DDeviceManager9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DDeviceManager9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DDeviceManager9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle">CloseDeviceHandle</a>
</td>
<td align="left" width="63%">
Closes a Direct3D device handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice">GetVideoService</a>
</td>
<td align="left" width="63%">
Gets a DirectX Video Acceleration (DXVA) service interface.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice">LockDevice</a>
</td>
<td align="left" width="63%">
Gives the caller exclusive access to the Direct3D device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle">OpenDeviceHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the Direct3D device.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">ResetDevice</a>
</td>
<td align="left" width="63%">
Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice">TestDevice</a>
</td>
<td align="left" width="63%">
Tests whether a Direct3D device handle is valid.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice">UnlockDevice</a>
</td>
<td align="left" width="63%">
Unlocks the Direct3D device.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>. To create the Direct3D device manager, call <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9">DXVA2CreateDirect3DDeviceManager9</a>.

To get this interface from the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR), call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service GUID is <b>MR_VIDEO_ACCELERATION_SERVICE</b>. For the DirectShow EVR filter, call <b>GetService</b> on the filter's pins.

The Direct3D Device Manager supports Direct3D 9 devices only. It does not support DXGI devices.

Windows Store apps must use <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> and <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-apis">Direct3D 11 Video APIs</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

