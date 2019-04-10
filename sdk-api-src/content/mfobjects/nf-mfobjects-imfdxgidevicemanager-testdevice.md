---
UID: NF:mfobjects.IMFDXGIDeviceManager.TestDevice
title: IMFDXGIDeviceManager::TestDevice (mfobjects.h)
author: windows-sdk-content
description: Tests whether a Microsoft Direct3D device handle is valid.
old-location: mf\imfdxgidevicemanager_testdevice.htm
tech.root: medfound
ms.assetid: DBBECFE0-110D-4A77-88D4-7D6AB8B2A67C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],TestDevice method, IMFDXGIDeviceManager.TestDevice, IMFDXGIDeviceManager::TestDevice, TestDevice, TestDevice method [Media Foundation], TestDevice method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_testdevice, mfobjects/IMFDXGIDeviceManager::TestDevice
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
 - IMFDXGIDeviceManager.TestDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDXGIDeviceManager::TestDevice


## -description


Tests whether a Microsoft Direct3D device handle is valid.


## -parameters




### -param hDevice [in]

A handle to the Direct3D device. To get the device handle, call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">IMFDXGIDeviceManager::OpenDeviceHandle</a>.


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
<dt><b>MF_E_DXGI_NEW_VIDEO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device handle is invalid. 


</td>
</tr>
</table>
 




## -remarks



If the method returns <b>MF_E_DXGI_NEW_VIDEO_DEVICE</b>, call <a href="https://msdn.microsoft.com/D5C74D6C-F066-4905-9D02-886FA503F58E">IMFDXGIDeviceManager::CloseDeviceHandle</a> to close the handle and then call <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">OpenDeviceHandle</a> again to get a new handle. The  <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a> method invalidates all open device handles.




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

