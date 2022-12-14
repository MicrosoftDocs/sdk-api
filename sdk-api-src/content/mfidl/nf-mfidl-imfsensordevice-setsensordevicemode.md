---
UID: NF:mfidl.IMFSensorDevice.SetSensorDeviceMode
title: IMFSensorDevice::SetSensorDeviceMode (mfidl.h)
description: Sets a value that specifies the sharing mode of the sensor device to either controller or shared.
helpviewer_keywords: ["IMFSensorDevice interface [Media Foundation]","SetSensorDeviceMode method","IMFSensorDevice.SetSensorDeviceMode","IMFSensorDevice::SetSensorDeviceMode","SetSensorDeviceMode","SetSensorDeviceMode method [Media Foundation]","SetSensorDeviceMode method [Media Foundation]","IMFSensorDevice interface","mf.imfsensordevice_setsensordevicemode","mfidl/IMFSensorDevice::SetSensorDeviceMode"]
old-location: mf\imfsensordevice_setsensordevicemode.htm
tech.root: mf
ms.assetid: 2B0DC098-EA3B-4061-8191-C67BA54663A3
ms.date: 12/05/2018
ms.keywords: IMFSensorDevice interface [Media Foundation],SetSensorDeviceMode method, IMFSensorDevice.SetSensorDeviceMode, IMFSensorDevice::SetSensorDeviceMode, SetSensorDeviceMode, SetSensorDeviceMode method [Media Foundation], SetSensorDeviceMode method [Media Foundation],IMFSensorDevice interface, mf.imfsensordevice_setsensordevicemode, mfidl/IMFSensorDevice::SetSensorDeviceMode
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
 - IMFSensorDevice::SetSensorDeviceMode
 - mfidl/IMFSensorDevice::SetSensorDeviceMode
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
 - IMFSensorDevice.SetSensorDeviceMode
---

# IMFSensorDevice::SetSensorDeviceMode


## -description

Sets a value that specifies the sharing mode of the sensor device to either controller or shared.

## -parameters

### -param eMode [in]

A member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensordevicemode">MFSensorDeviceMode</a> enumeration specifying whether the device is in shared or controller mode.

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