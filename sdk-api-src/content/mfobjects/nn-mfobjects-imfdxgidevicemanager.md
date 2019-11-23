---
UID: NN:mfobjects.IMFDXGIDeviceManager
title: IMFDXGIDeviceManager (mfobjects.h)

description: Enables two threads to share the same Microsoft Direct3D 11 device.
old-location: mf\imfdxgidevicemanager.htm
tech.root: medfound
ms.assetid: 4A0DC266-FCF0-4ECD-AC78-CF429839486D

ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager, IMFDXGIDeviceManager interface [Media Foundation], IMFDXGIDeviceManager interface [Media Foundation],described, mf.imfdxgidevicemanager, mfobjects/IMFDXGIDeviceManager
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFDXGIDeviceManager"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFDXGIDeviceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDXGIDeviceManager interface


## -description


Enables two threads to share the same Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDXGIDeviceManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDXGIDeviceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDXGIDeviceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-closedevicehandle">CloseDeviceHandle</a>
</td>
<td align="left" width="63%">
Closes a Direct3D device handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-getvideoservice">GetVideoService</a>
</td>
<td align="left" width="63%">
Queries the Direct3D device for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-lockdevice">LockDevice</a>
</td>
<td align="left" width="63%">
Gives the caller exclusive access to the Direct3D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle">OpenDeviceHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the Direct3D device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">ResetDevice</a>
</td>
<td align="left" width="63%">
Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-testdevice">TestDevice</a>
</td>
<td align="left" width="63%">
Tests whether a Direct3D device handle is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-unlockdevice">UnlockDevice</a>
</td>
<td align="left" width="63%">
Unlocks the Direct3D device.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager. To create the DXGI Device Manager, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgidevicemanager">MFCreateDXGIDeviceManager</a> function.

When you create an <b>IMFDXGIDeviceManager</b> with <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgidevicemanager">MFCreateDXGIDeviceManager</a>, a Direct3D 11 device is not associated with the device manager. To associate a Direct3D 11 device with the device manager, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>, passing in the pointer to the Direct3D 11 device. To create a Direct3D 11 device, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>. The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a> enumeration.

For Microsoft Direct3D 9 devices, use the <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9">IDirect3DDeviceManager9</a> interface.

Windows Store apps must use <b>IMFDXGIDeviceManager</b> and <a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-apis">Direct3D 11 Video APIs</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

