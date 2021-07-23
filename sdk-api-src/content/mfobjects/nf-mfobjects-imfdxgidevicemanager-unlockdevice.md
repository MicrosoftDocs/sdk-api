---
UID: NF:mfobjects.IMFDXGIDeviceManager.UnlockDevice
title: IMFDXGIDeviceManager::UnlockDevice (mfobjects.h)
description: Unlocks the Microsoft Direct3D device.
helpviewer_keywords: ["IMFDXGIDeviceManager interface [Media Foundation]","UnlockDevice method","IMFDXGIDeviceManager.UnlockDevice","IMFDXGIDeviceManager::UnlockDevice","UnlockDevice","UnlockDevice method [Media Foundation]","UnlockDevice method [Media Foundation]","IMFDXGIDeviceManager interface","mf.imfdxgidevicemanager_unlockdevice","mfobjects/IMFDXGIDeviceManager::UnlockDevice"]
old-location: mf\imfdxgidevicemanager_unlockdevice.htm
tech.root: mf
ms.assetid: DE6A8E16-BC25-4B7C-B95D-A46D7C0870E3
ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],UnlockDevice method, IMFDXGIDeviceManager.UnlockDevice, IMFDXGIDeviceManager::UnlockDevice, UnlockDevice, UnlockDevice method [Media Foundation], UnlockDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_unlockdevice, mfobjects/IMFDXGIDeviceManager::UnlockDevice
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
 - IMFDXGIDeviceManager::UnlockDevice
 - mfobjects/IMFDXGIDeviceManager::UnlockDevice
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
 - IMFDXGIDeviceManager.UnlockDevice
---

# IMFDXGIDeviceManager::UnlockDevice


## -description

Unlocks the Microsoft Direct3D device.

## -parameters

### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle">IMFDXGIDeviceManager::OpenDeviceHandle</a>.

### -param fSaveState [in]

Reserved.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Call this method to release the device after calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-lockdevice">IMFDXGIDeviceManager::LockDevice</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>