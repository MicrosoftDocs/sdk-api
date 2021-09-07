---
UID: NN:dxva2api.IDirect3DDeviceManager9
title: IDirect3DDeviceManager9 (dxva2api.h)
description: Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.
helpviewer_keywords: ["IDirect3DDeviceManager9","IDirect3DDeviceManager9 interface [Media Foundation]","IDirect3DDeviceManager9 interface [Media Foundation]","described","dxva2api/IDirect3DDeviceManager9","e661e666-dc51-4a71-9ecd-62a667bb217d","mf.idirect3ddevicemanager9"]
old-location: mf\idirect3ddevicemanager9.htm
tech.root: mf
ms.assetid: e661e666-dc51-4a71-9ecd-62a667bb217d
ms.date: 12/05/2018
ms.keywords: IDirect3DDeviceManager9, IDirect3DDeviceManager9 interface [Media Foundation], IDirect3DDeviceManager9 interface [Media Foundation],described, dxva2api/IDirect3DDeviceManager9, e661e666-dc51-4a71-9ecd-62a667bb217d, mf.idirect3ddevicemanager9
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
 - IDirect3DDeviceManager9
 - dxva2api/IDirect3DDeviceManager9
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
 - IDirect3DDeviceManager9
---

# IDirect3DDeviceManager9 interface


## -description

Enables two threads to share the same Direct3D 9 device, and provides access to the DirectX Video Acceleration (DXVA) features of the device.

## -inheritance

The <b>IDirect3DDeviceManager9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DDeviceManager9</b> also has these types of members:

## -remarks

This interface is exposed by the <a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>. To create the Direct3D device manager, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9">DXVA2CreateDirect3DDeviceManager9</a>.

To get this interface from the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR), call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service GUID is <b>MR_VIDEO_ACCELERATION_SERVICE</b>. For the DirectShow EVR filter, call <b>GetService</b> on the filter's pins.

The Direct3D Device Manager supports Direct3D 9 devices only. It does not support DXGI devices.

Windows Store apps must use <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> and <a href="/windows/desktop/medfound/direct3d-11-video-apis">Direct3D 11 Video APIs</a>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-device-manager">Direct3D Device Manager</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
