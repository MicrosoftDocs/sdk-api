---
UID: NN:mfobjects.IMFDXGIDeviceManager
title: IMFDXGIDeviceManager (mfobjects.h)
author: windows-sdk-content
description: Enables two threads to share the same Microsoft Direct3D 11 device.
old-location: mf\imfdxgidevicemanager.htm
tech.root: medfound
ms.assetid: 4A0DC266-FCF0-4ECD-AC78-CF429839486D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager, IMFDXGIDeviceManager interface [Media Foundation], IMFDXGIDeviceManager interface [Media Foundation],described, mf.imfdxgidevicemanager, mfobjects/IMFDXGIDeviceManager
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDXGIDeviceManager interface


## -description


Enables two threads to share the same Microsoft Direct3D 11 device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDXGIDeviceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFDXGIDeviceManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D5C74D6C-F066-4905-9D02-886FA503F58E">CloseDeviceHandle</a>
</td>
<td align="left" width="63%">
Closes a Direct3D device handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B0C7C31B-39AF-48B6-8D86-F4DFCC546CDE">GetVideoService</a>
</td>
<td align="left" width="63%">
Queries the Direct3D device for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EFB458D5-40A9-4729-9C22-B66FE76D5680">LockDevice</a>
</td>
<td align="left" width="63%">
Gives the caller exclusive access to the Direct3D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">OpenDeviceHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the Direct3D device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">ResetDevice</a>
</td>
<td align="left" width="63%">
Sets the Direct3D device or notifies the device manager that the Direct3D device was reset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DBBECFE0-110D-4A77-88D4-7D6AB8B2A67C">TestDevice</a>
</td>
<td align="left" width="63%">
Tests whether a Direct3D device handle is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE6A8E16-BC25-4B7C-B95D-A46D7C0870E3">UnlockDevice</a>
</td>
<td align="left" width="63%">
Unlocks the Direct3D device.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager. To create the DXGI Device Manager, call the <a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a> function.

When you create an <b>IMFDXGIDeviceManager</b> with <a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a>, a Direct3D 11 device is not associated with the device manager. To associate a Direct3D 11 device with the device manager, call <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>, passing in the pointer to the Direct3D 11 device. To create a Direct3D 11 device, call <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>. The device should be created with the <b>D3D11_CREATE_DEVICE_VIDEO_SUPPORT</b> device creation flag which is defined in the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_FLAG</a> enumeration.

For Microsoft Direct3D 9 devices, use the <a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a> interface.

Windows Store apps must use <b>IMFDXGIDeviceManager</b> and <a href="https://msdn.microsoft.com/7C91BEB9-53D2-4799-98F8-2B92128E37C3">Direct3D 11 Video APIs</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

