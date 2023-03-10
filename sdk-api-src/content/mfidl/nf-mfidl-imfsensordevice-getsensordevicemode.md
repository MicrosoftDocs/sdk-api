---
UID: NF:mfidl.IMFSensorDevice.GetSensorDeviceMode
title: IMFSensorDevice::GetSensorDeviceMode (mfidl.h)
description: Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.
helpviewer_keywords: ["GetSensorDeviceMode","GetSensorDeviceMode method [Media Foundation]","GetSensorDeviceMode method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetSensorDeviceMode method","IMFSensorDevice.GetSensorDeviceMode","IMFSensorDevice::GetSensorDeviceMode","mf.imfsensordevice_getsensordevicemode","mfidl/IMFSensorDevice::GetSensorDeviceMode"]
old-location: mf\imfsensordevice_getsensordevicemode.htm
tech.root: mf
ms.assetid: 21594884-DAA5-450C-855D-E800FE164C5E
ms.date: 12/05/2018
ms.keywords: GetSensorDeviceMode, GetSensorDeviceMode method [Media Foundation], GetSensorDeviceMode method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetSensorDeviceMode method, IMFSensorDevice.GetSensorDeviceMode, IMFSensorDevice::GetSensorDeviceMode, mf.imfsensordevice_getsensordevicemode, mfidl/IMFSensorDevice::GetSensorDeviceMode
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
 - IMFSensorDevice::GetSensorDeviceMode
 - mfidl/IMFSensorDevice::GetSensorDeviceMode
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
 - IMFSensorDevice.GetSensorDeviceMode
---

# IMFSensorDevice::GetSensorDeviceMode


## -description

Gets a value that specifies the current sharing mode of the sensor device, which is either controller or shared.

## -parameters

### -param peMode

If the call succeeds, receives a member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensordevicemode">MFSensorDeviceMode</a>, specifying the current mode of the sendsor device.

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