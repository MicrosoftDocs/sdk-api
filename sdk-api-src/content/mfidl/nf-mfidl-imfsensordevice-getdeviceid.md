---
UID: NF:mfidl.IMFSensorDevice.GetDeviceId
title: IMFSensorDevice::GetDeviceId (mfidl.h)
description: Gets the unique identifier for the device. This value is currently unused.
helpviewer_keywords: ["GetDeviceId","GetDeviceId method [Media Foundation]","GetDeviceId method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetDeviceId method","IMFSensorDevice.GetDeviceId","IMFSensorDevice::GetDeviceId","mf.imfsensordevice_getdeviceid","mfidl/IMFSensorDevice::GetDeviceId"]
old-location: mf\imfsensordevice_getdeviceid.htm
tech.root: mf
ms.assetid: 90598DC7-A4FB-4C3F-A671-1549703AC9DB
ms.date: 12/05/2018
ms.keywords: GetDeviceId, GetDeviceId method [Media Foundation], GetDeviceId method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetDeviceId method, IMFSensorDevice.GetDeviceId, IMFSensorDevice::GetDeviceId, mf.imfsensordevice_getdeviceid, mfidl/IMFSensorDevice::GetDeviceId
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorDevice::GetDeviceId
 - mfidl/IMFSensorDevice::GetDeviceId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorDevice.GetDeviceId
---

# IMFSensorDevice::GetDeviceId


## -description

Gets the unique identifier for the device. This value is currently unused.

## -parameters

### -param pDeviceId [out]

The unique identifier for the device.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDeviceId</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor group has not been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>