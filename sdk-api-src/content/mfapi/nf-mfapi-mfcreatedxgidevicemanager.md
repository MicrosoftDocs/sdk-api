---
UID: NF:mfapi.MFCreateDXGIDeviceManager
title: MFCreateDXGIDeviceManager function (mfapi.h)
description: Creates an instance of the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.
helpviewer_keywords: ["MFCreateDXGIDeviceManager","MFCreateDXGIDeviceManager function [Media Foundation]","mf.mfcreatedxgidevicemanager","mfapi/MFCreateDXGIDeviceManager"]
old-location: mf\mfcreatedxgidevicemanager.htm
tech.root: mf
ms.assetid: 5398B6D7-1E7D-4987-A163-3360C805EE9C
ms.date: 12/05/2018
ms.keywords: MFCreateDXGIDeviceManager, MFCreateDXGIDeviceManager function [Media Foundation], mf.mfcreatedxgidevicemanager, mfapi/MFCreateDXGIDeviceManager
req.header: mfapi.h
req.include-header: 
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateDXGIDeviceManager
 - mfapi/MFCreateDXGIDeviceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateDXGIDeviceManager
---

# MFCreateDXGIDeviceManager function


## -description

Creates an instance of the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.

## -parameters

### -param resetToken [out]

Receives a token that identifies this instance of the DXGI Device Manager. Use this token when calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>.

### -param ppDeviceManager [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When you create an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> with <b>MFCreateDXGIDeviceManager</b>, a Microsoft Direct3D 11 device is not associated with the device manager. To associate a Direct3D 11 device with the device manager, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>, passing in the pointer to the Direct3D 11 device. To create a Direct3D 11 device, call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>. The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a> enumeration.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>