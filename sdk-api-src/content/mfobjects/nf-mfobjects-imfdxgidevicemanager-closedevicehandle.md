---
UID: NF:mfobjects.IMFDXGIDeviceManager.CloseDeviceHandle
title: IMFDXGIDeviceManager::CloseDeviceHandle
author: windows-sdk-content
description: Closes a Microsoft Direct3D device handle.
old-location: mf\imfdxgidevicemanager_closedevicehandle.htm
old-project: medfound
ms.assetid: D5C74D6C-F066-4905-9D02-886FA503F58E
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: CloseDeviceHandle, CloseDeviceHandle method [Media Foundation], CloseDeviceHandle method [Media Foundation],IMFDXGIDeviceManager interface, IMFDXGIDeviceManager interface [Media Foundation],CloseDeviceHandle method, IMFDXGIDeviceManager.CloseDeviceHandle, IMFDXGIDeviceManager::CloseDeviceHandle, mf.imfdxgidevicemanager_closedevicehandle, mfobjects/IMFDXGIDeviceManager::CloseDeviceHandle
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFDXGIDeviceManager.CloseDeviceHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDXGIDeviceManager::CloseDeviceHandle


## -description


Closes a Microsoft Direct3D device handle.


## -parameters




### -param hDevice [in]

A handle to the Direct3D device.




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
</table>
 




## -remarks



  Call this method to release a device handle that was retrieved by the <a href="https://msdn.microsoft.com/B025DF73-1F85-46F3-9AD4-2385BD515DDD">IMFDXGIDeviceManager::OpenDeviceHandle</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a>
 

 

