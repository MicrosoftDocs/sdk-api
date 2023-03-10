---
UID: NF:mfidl.IMFSensorDevice.GetDeviceAttributes
title: IMFSensorDevice::GetDeviceAttributes (mfidl.h)
description: Gets the IMFAttributes for the sensor group.
helpviewer_keywords: ["GetDeviceAttributes","GetDeviceAttributes method [Media Foundation]","GetDeviceAttributes method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetDeviceAttributes method","IMFSensorDevice.GetDeviceAttributes","IMFSensorDevice::GetDeviceAttributes","mf.imfsensordevice_getdeviceattributes","mfidl/IMFSensorDevice::GetDeviceAttributes"]
old-location: mf\imfsensordevice_getdeviceattributes.htm
tech.root: mf
ms.assetid: 4F509D34-23C3-4034-8D89-0A2E0651F235
ms.date: 12/05/2018
ms.keywords: GetDeviceAttributes, GetDeviceAttributes method [Media Foundation], GetDeviceAttributes method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetDeviceAttributes method, IMFSensorDevice.GetDeviceAttributes, IMFSensorDevice::GetDeviceAttributes, mf.imfsensordevice_getdeviceattributes, mfidl/IMFSensorDevice::GetDeviceAttributes
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
 - IMFSensorDevice::GetDeviceAttributes
 - mfidl/IMFSensorDevice::GetDeviceAttributes
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
 - IMFSensorDevice.GetDeviceAttributes
---

# IMFSensorDevice::GetDeviceAttributes


## -description

Gets the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the sensor group.

## -parameters

### -param ppAttributes [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface representing the internal attribute store of the sensor device.

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
The <i>ppAttributes</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The sensor device has not been initialized.

</td>
</tr>
</table>

## -remarks

The object returned is a copy of the internal attribute store and so changes made to the returned attributes have no effect on the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>