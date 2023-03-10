---
UID: NF:mfidl.IMFSensorDevice.GetFlags
title: IMFSensorDevice::GetFlags (mfidl.h)
description: Gets the flags set for the sensor device. This method is reserved for future use.
helpviewer_keywords: ["GetFlags","GetFlags method [Media Foundation]","GetFlags method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetFlags method","IMFSensorDevice.GetFlags","IMFSensorDevice::GetFlags","mf.imfsensordevice_getflags","mfidl/IMFSensorDevice::GetFlags"]
old-location: mf\imfsensordevice_getflags.htm
tech.root: mf
ms.assetid: 802649EE-7A24-429A-92DB-775A215BCD79
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetFlags method, IMFSensorDevice.GetFlags, IMFSensorDevice::GetFlags, mf.imfsensordevice_getflags, mfidl/IMFSensorDevice::GetFlags
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
 - IMFSensorDevice::GetFlags
 - mfidl/IMFSensorDevice::GetFlags
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
 - IMFSensorDevice.GetFlags
---

# IMFSensorDevice::GetFlags


## -description

Gets the flags set for the sensor device. This method is reserved for future use.

## -parameters

### -param pFlags [out]

The flags set for the sensor device.

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

## -remarks

This method is reserved for future use and should not be called.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>