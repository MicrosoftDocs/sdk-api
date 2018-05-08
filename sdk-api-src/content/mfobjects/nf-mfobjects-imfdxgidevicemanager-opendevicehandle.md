---
UID: NF:mfobjects.IMFDXGIDeviceManager.OpenDeviceHandle
title: IMFDXGIDeviceManager::OpenDeviceHandle
author: windows-driver-content
description: Gets a handle to the Microsoft Direct3D device.
old-location: mf\imfdxgidevicemanager_opendevicehandle.htm
old-project: medfound
ms.assetid: B025DF73-1F85-46F3-9AD4-2385BD515DDD
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],OpenDeviceHandle method, IMFDXGIDeviceManager.OpenDeviceHandle, IMFDXGIDeviceManager::OpenDeviceHandle, OpenDeviceHandle, OpenDeviceHandle method [Media Foundation], OpenDeviceHandle method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_opendevicehandle, mfobjects/IMFDXGIDeviceManager::OpenDeviceHandle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfobjects.h
api_name:
-	IMFDXGIDeviceManager.OpenDeviceHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDXGIDeviceManager::OpenDeviceHandle


## -description


Gets a handle to the Microsoft Direct3D device. 


## -parameters




### -param phDevice [out]

Receives the device handle.


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
<dt><b>MF_E_DXGI_DEVICE_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The DXGI Device Manager was not initialized. The owner of the device must call <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

