---
UID: NF:mfidl.IMFSensorDevice.GetDeviceType
title: IMFSensorDevice::GetDeviceType (mfidl.h)
description: Gets a value that specifies the type of sensor device represented by the object.
helpviewer_keywords: ["GetDeviceType","GetDeviceType method [Media Foundation]","GetDeviceType method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetDeviceType method","IMFSensorDevice.GetDeviceType","IMFSensorDevice::GetDeviceType","mf.imfsensordevice_getdevicetype","mfidl/IMFSensorDevice::GetDeviceType"]
old-location: mf\imfsensordevice_getdevicetype.htm
tech.root: mf
ms.assetid: 6714B5A8-83F2-44CD-B061-749EA6BFBF20
ms.date: 12/05/2018
ms.keywords: GetDeviceType, GetDeviceType method [Media Foundation], GetDeviceType method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetDeviceType method, IMFSensorDevice.GetDeviceType, IMFSensorDevice::GetDeviceType, mf.imfsensordevice_getdevicetype, mfidl/IMFSensorDevice::GetDeviceType
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
 - IMFSensorDevice::GetDeviceType
 - mfidl/IMFSensorDevice::GetDeviceType
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
 - IMFSensorDevice.GetDeviceType
---

# IMFSensorDevice::GetDeviceType


## -description

Gets a value that specifies the type of sensor device represented by the object.

## -parameters

### -param pType

A value that specifies the type of sensor device represented by the object.

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
The <i>pType</i> parameter is null.

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