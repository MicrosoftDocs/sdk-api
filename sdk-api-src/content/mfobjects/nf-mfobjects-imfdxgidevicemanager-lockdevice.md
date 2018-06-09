---
UID: NF:mfobjects.IMFDXGIDeviceManager.LockDevice
title: IMFDXGIDeviceManager::LockDevice
author: windows-sdk-content
description: Gives the caller exclusive access to the Microsoft Direct3D device.
old-location: mf\imfdxgidevicemanager_lockdevice.htm
old-project: medfound
ms.assetid: EFB458D5-40A9-4729-9C22-B66FE76D5680
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],LockDevice method, IMFDXGIDeviceManager.LockDevice, IMFDXGIDeviceManager::LockDevice, LockDevice, LockDevice method [Media Foundation], LockDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_lockdevice, mfobjects/IMFDXGIDeviceManager::LockDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFDXGIDeviceManager.LockDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDXGIDeviceManager::LockDevice


## -description


Gives the caller exclusive access to the Microsoft Direct3D device.


## -parameters




### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">IMFDXGIDeviceManager::OpenDeviceHandle</a>.


### -param riid [in]

The interface identifier (IID) of the requested interface. The Direct3D device will support the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
</li>
</ul>

### -param ppUnkDevice [out]

Receives a pointer to the requested interface. The caller must release the interface.


### -param fBlock [in]

Specifies whether to wait for the device lock. If the device is already locked and this parameter is <b>TRUE</b>, the method blocks until the device is unlocked. Otherwise, if the device is locked and this parameter is <b>FALSE</b>, the method returns immediately with the error code <b>DXVA2_E_VIDEO_DEVICE_LOCKED</b>.


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
The DXGI Device Manager was not initialized. The owner of the device must call <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>.

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
<dt><b>MF_E_DXGI_VIDEO_DEVICE_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The device is locked and <i>fBlock</i> is <b>FALSE</b>. 


</td>
</tr>
</table>
 




## -remarks



When you are done using the Direct3D device, call <a href="https://msdn.microsoft.com/DE6A8E16-BC25-4B7C-B95D-A46D7C0870E3">IMFDXGIDeviceManager::UnlockDevice</a> to unlock the device.

If the method returns <b>MF_E_DXGI_NEW_VIDEO_DEVICE</b>, call <a href="https://msdn.microsoft.com/D5C74D6C-F066-4905-9D02-886FA503F58E">IMFDXGIDeviceManager::CloseDeviceHandle</a> to close the handle and then call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">OpenDeviceHandle</a> again to get a new handle. The  <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a> method invalidates all open device handles.

If <i>fBlock</i> is <b>TRUE</b>, this method can potentially deadlock. For example, it will deadlock if a thread calls <b>LockDevice</b> and then waits on another thread that calls <b>LockDevice</b>. It will also deadlock if a thread calls <b>LockDevice</b> twice without calling <a href="https://msdn.microsoft.com/DE6A8E16-BC25-4B7C-B95D-A46D7C0870E3">UnlockDevice</a> in between. 






## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

