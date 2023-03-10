---
UID: NF:mfobjects.IMFDXGIDeviceManager.CloseDeviceHandle
title: IMFDXGIDeviceManager::CloseDeviceHandle (mfobjects.h)
description: Closes a Microsoft Direct3D device handle.
helpviewer_keywords: ["CloseDeviceHandle","CloseDeviceHandle method [Media Foundation]","CloseDeviceHandle method [Media Foundation]","IMFDXGIDeviceManager interface","IMFDXGIDeviceManager interface [Media Foundation]","CloseDeviceHandle method","IMFDXGIDeviceManager.CloseDeviceHandle","IMFDXGIDeviceManager::CloseDeviceHandle","mf.imfdxgidevicemanager_closedevicehandle","mfobjects/IMFDXGIDeviceManager::CloseDeviceHandle"]
old-location: mf\imfdxgidevicemanager_closedevicehandle.htm
tech.root: mf
ms.assetid: D5C74D6C-F066-4905-9D02-886FA503F58E
ms.date: 12/05/2018
ms.keywords: CloseDeviceHandle, CloseDeviceHandle method [Media Foundation], CloseDeviceHandle method [Media Foundation],IMFDXGIDeviceManager interface, IMFDXGIDeviceManager interface [Media Foundation],CloseDeviceHandle method, IMFDXGIDeviceManager.CloseDeviceHandle, IMFDXGIDeviceManager::CloseDeviceHandle, mf.imfdxgidevicemanager_closedevicehandle, mfobjects/IMFDXGIDeviceManager::CloseDeviceHandle
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
 - IMFDXGIDeviceManager::CloseDeviceHandle
 - mfobjects/IMFDXGIDeviceManager::CloseDeviceHandle
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
 - IMFDXGIDeviceManager.CloseDeviceHandle
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

  Call this method to release a device handle that was retrieved by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-opendevicehandle">IMFDXGIDeviceManager::OpenDeviceHandle</a> method.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>