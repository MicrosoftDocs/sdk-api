---
UID: NF:mfobjects.IMFDXGIDeviceManager.ResetDevice
title: IMFDXGIDeviceManager::ResetDevice (mfobjects.h)
description: Sets the Microsoft Direct3D device or notifies the device manager that the Direct3D device was reset.
helpviewer_keywords: ["IMFDXGIDeviceManager interface [Media Foundation]","ResetDevice method","IMFDXGIDeviceManager.ResetDevice","IMFDXGIDeviceManager::ResetDevice","ResetDevice","ResetDevice method [Media Foundation]","ResetDevice method [Media Foundation]","IMFDXGIDeviceManager interface","mf.imfdxgidevicemanager_resetdevice","mfobjects/IMFDXGIDeviceManager::ResetDevice"]
old-location: mf\imfdxgidevicemanager_resetdevice.htm
tech.root: mf
ms.assetid: D8A2291A-792B-4D24-997A-9C152FFE5426
ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],ResetDevice method, IMFDXGIDeviceManager.ResetDevice, IMFDXGIDeviceManager::ResetDevice, ResetDevice, ResetDevice method [Media Foundation], ResetDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_resetdevice, mfobjects/IMFDXGIDeviceManager::ResetDevice
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
 - IMFDXGIDeviceManager::ResetDevice
 - mfobjects/IMFDXGIDeviceManager::ResetDevice
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
 - IMFDXGIDeviceManager.ResetDevice
---

# IMFDXGIDeviceManager::ResetDevice


## -description

Sets the Microsoft Direct3D device or notifies the device manager that the Direct3D device was reset.

## -parameters

### -param pUnkDevice [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the DXGI device.

### -param resetToken [in]

The token that was received in the <i>pResetToken</i> parameter of the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgidevicemanager">MFCreateDXGIDeviceManager</a> function.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When you first create the DXGI Device Manager, call this method with a pointer to the Direct3D device. (The device manager does not create the device; the caller must provide the device pointer initially.) Also call this method if the Direct3D device becomes lost and you need to reset the device or create a new device. 

The <i>resetToken</i> parameter ensures that only the component that originally created the device manager can invalidate the current device.

If this method succeeds, all open device handles become invalid.

To create a Microsoft Direct3D 11 device, call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>. 

The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a> enumeration.

It is recommended that you use multi-thread protection on the device context to prevent deadlock issues that can sometimes happen when you call<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer"> ID3D11VideoContext::GetDecoderBuffer</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-releasedecoderbuffer">ID3D11VideoContext::ReleaseDecoderBuffer</a>. To set multi-thread protection, first call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> to get an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10multithread">ID3D10Multithread</a> pointer. Then call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10multithread-setmultithreadprotected">ID3D10Multithread::SetMultithreadProtected</a>, passing in <b>true</b> for <i>bMTProtect</i>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>