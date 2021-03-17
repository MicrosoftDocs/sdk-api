---
UID: NF:mfobjects.IMFDXGIDeviceManager.OpenDeviceHandle
title: IMFDXGIDeviceManager::OpenDeviceHandle (mfobjects.h)
description: Gets a handle to the Microsoft Direct3D device.
helpviewer_keywords: ["IMFDXGIDeviceManager interface [Media Foundation]","OpenDeviceHandle method","IMFDXGIDeviceManager.OpenDeviceHandle","IMFDXGIDeviceManager::OpenDeviceHandle","OpenDeviceHandle","OpenDeviceHandle method [Media Foundation]","OpenDeviceHandle method [Media Foundation]","IMFDXGIDeviceManager interface","mf.imfdxgidevicemanager_opendevicehandle","mfobjects/IMFDXGIDeviceManager::OpenDeviceHandle"]
old-location: mf\imfdxgidevicemanager_opendevicehandle.htm
tech.root: mf
ms.assetid: B025DF73-1F85-46F3-9AD4-2385BD515DDD
ms.date: 12/05/2018
ms.keywords: IMFDXGIDeviceManager interface [Media Foundation],OpenDeviceHandle method, IMFDXGIDeviceManager.OpenDeviceHandle, IMFDXGIDeviceManager::OpenDeviceHandle, OpenDeviceHandle, OpenDeviceHandle method [Media Foundation], OpenDeviceHandle method [Media Foundation],IMFDXGIDeviceManager interface, mf.imfdxgidevicemanager_opendevicehandle, mfobjects/IMFDXGIDeviceManager::OpenDeviceHandle
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
 - IMFDXGIDeviceManager::OpenDeviceHandle
 - mfobjects/IMFDXGIDeviceManager::OpenDeviceHandle
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
 - IMFDXGIDeviceManager.OpenDeviceHandle
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
The DXGI Device Manager was not initialized. The owner of the device must call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgidevicemanager-resetdevice">IMFDXGIDeviceManager::ResetDevice</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>