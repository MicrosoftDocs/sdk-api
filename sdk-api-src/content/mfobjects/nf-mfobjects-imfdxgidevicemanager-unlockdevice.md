---
UID: NF:mfobjects.IMFDXGIDeviceManager.UnlockDevice
title: IMFDXGIDeviceManager::UnlockDevice
author: windows-sdk-content
description: Unlocks the Microsoft Direct3D device.
old-location: mf\imfdxgidevicemanager_unlockdevice.htm
tech.root: medfound
ms.assetid: DE6A8E16-BC25-4B7C-B95D-A46D7C0870E3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],UnlockDevice method, IMFDXGIDeviceManager.UnlockDevice, IMFDXGIDeviceManager::UnlockDevice, UnlockDevice, UnlockDevice method [Media Foundation], UnlockDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_unlockdevice, mfobjects/IMFDXGIDeviceManager::UnlockDevice
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
 - IMFDXGIDeviceManager.UnlockDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIDeviceManager::UnlockDevice


## -description


Unlocks the Microsoft Direct3D device.


## -parameters




### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">IMFDXGIDeviceManager::OpenDeviceHandle</a>.


### -param fSaveState [in]

Reserved.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Call this method to release the device after calling <a href="https://msdn.microsoft.com/EFB458D5-40A9-4729-9C22-B66FE76D5680">IMFDXGIDeviceManager::LockDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

