---
UID: NF:mfobjects.IMFDXGIDeviceManager.GetVideoService
title: IMFDXGIDeviceManager::GetVideoService
author: windows-sdk-content
description: Queries the Microsoft Direct3D device for an interface.
old-location: mf\imfdxgidevicemanager_getvideoservice.htm
tech.root: medfound
ms.assetid: B0C7C31B-39AF-48B6-8D86-F4DFCC546CDE
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetVideoService, GetVideoService method [Media Foundation], GetVideoService method [Media Foundation],IMFDXGIDeviceManager interface, IMFDXGIDeviceManager interface [Media Foundation],GetVideoService method, IMFDXGIDeviceManager.GetVideoService, IMFDXGIDeviceManager::GetVideoService, mf.imfdxgidevicemanager_getvideoservice, mfobjects/IMFDXGIDeviceManager::GetVideoService
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
 - IMFDXGIDeviceManager.GetVideoService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIDeviceManager::GetVideoService


## -description


Queries the Microsoft Direct3D device for an interface.


## -parameters




### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">IMFDXGIDeviceManager::OpenDeviceHandle</a>.


### -param riid [in]

The interface identifier (IID) of the requested interface. The Direct3D device supports the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>. To get a pointer to the Direct3D11 device, use <b>IID_ID3D11Device</b> as the <i>riid</i>.</li>
<li>
<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>. To get a pointer to the Direct3D11 video device, use <b>IID_ID3D11VideoDevice</b> as the <i>riid</i>.</li>
</ul>

### -param ppService [out]

Receives a pointer to the requested interface. The caller must release the interface.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
If a  <a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>  is specified and the D3D device created is using the reference rasterizer or WARP.  Or it is a hardware device and you are using the Microsoft Basic Display Adapter.

</td>
</tr>
</table>
 




## -remarks



If the method returns <b>MF_E_DXGI_NEW_VIDEO_DEVICE</b>, call <a href="https://msdn.microsoft.com/D5C74D6C-F066-4905-9D02-886FA503F58E">IMFDXGIDeviceManager::CloseDeviceHandle</a> to close the handle and then call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">OpenDeviceHandle</a> again to get a new handle. The  <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a> method invalidates all open device handles.

For more info see, <a href="https://msdn.microsoft.com/656556AA-0266-4318-9D3C-AED75BD728F6">Supporting Direct3D 11 Video Decoding in Media Foundation</a>.




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

