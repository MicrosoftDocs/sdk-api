---
UID: NF:mfobjects.IMFDXGIDeviceManager.ResetDevice
title: IMFDXGIDeviceManager::ResetDevice
author: windows-sdk-content
description: Sets the Microsoft Direct3D device or notifies the device manager that the Direct3D device was reset.
old-location: mf\imfdxgidevicemanager_resetdevice.htm
tech.root: medfound
ms.assetid: D8A2291A-792B-4D24-997A-9C152FFE5426
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],ResetDevice method, IMFDXGIDeviceManager.ResetDevice, IMFDXGIDeviceManager::ResetDevice, ResetDevice, ResetDevice method [Media Foundation], ResetDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_resetdevice, mfobjects/IMFDXGIDeviceManager::ResetDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFDXGIDeviceManager.ResetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIDeviceManager::ResetDevice


## -description


Sets the Microsoft Direct3D device or notifies the device manager that the Direct3D device was reset.


## -parameters




### -param pUnkDevice [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the DXGI device.


### -param resetToken [in]

The token that was received in the <i>pResetToken</i> parameter of the <a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a> function.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When you first create the DXGI Device Manager, call this method with a pointer to the Direct3D device. (The device manager does not create the device; the caller must provide the device pointer initially.) Also call this method if the Direct3D device becomes lost and you need to reset the device or create a new device. 

The <i>resetToken</i> parameter ensures that only the component that originally created the device manager can invalidate the current device.

If this method succeeds, all open device handles become invalid.

To create a Microsoft Direct3D 11 device, call <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>. 

The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_FLAG</a> enumeration.

It is recommended that you use multi-thread protection on the device context to prevent deadlock issues that can sometimes happen when you call<a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8"> ID3D11VideoContext::GetDecoderBuffer</a> or <a href="https://msdn.microsoft.com/C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0">ID3D11VideoContext::ReleaseDecoderBuffer</a>. To set multi-thread protection, first call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> to get an <a href="https://msdn.microsoft.com/en-us/library/Bb173816(v=VS.85).aspx">ID3D10Multithread</a> pointer. Then call <a href="https://msdn.microsoft.com/en-us/library/Bb173820(v=VS.85).aspx">ID3D10Multithread::SetMultithreadProtected</a>, passing in <b>true</b> for <i>bMTProtect</i>.




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

