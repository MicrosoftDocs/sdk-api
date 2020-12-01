---
UID: NF:mfidl.IMFSensorGroup.GetDefaultSensorDeviceIndex
title: IMFSensorGroup::GetDefaultSensorDeviceIndex (mfidl.h)
description: Retrieves the index of the default device in the sensor group.
helpviewer_keywords: ["GetDefaultSensorDeviceIndex","GetDefaultSensorDeviceIndex method [Media Foundation]","GetDefaultSensorDeviceIndex method [Media Foundation]","IMFSensorGroup interface","IMFSensorGroup interface [Media Foundation]","GetDefaultSensorDeviceIndex method","IMFSensorGroup.GetDefaultSensorDeviceIndex","IMFSensorGroup::GetDefaultSensorDeviceIndex","mf.imfsensorgroup_getdefaultsensordeviceindex","mfidl/IMFSensorGroup::GetDefaultSensorDeviceIndex"]
old-location: mf\imfsensorgroup_getdefaultsensordeviceindex.htm
tech.root: medfound
ms.assetid: E82A83F7-E984-4353-8CED-E3B5EE28EB3D
ms.date: 12/05/2018
ms.keywords: GetDefaultSensorDeviceIndex, GetDefaultSensorDeviceIndex method [Media Foundation], GetDefaultSensorDeviceIndex method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],GetDefaultSensorDeviceIndex method, IMFSensorGroup.GetDefaultSensorDeviceIndex, IMFSensorGroup::GetDefaultSensorDeviceIndex, mf.imfsensorgroup_getdefaultsensordeviceindex, mfidl/IMFSensorGroup::GetDefaultSensorDeviceIndex
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
 - IMFSensorGroup::GetDefaultSensorDeviceIndex
 - mfidl/IMFSensorGroup::GetDefaultSensorDeviceIndex
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
 - IMFSensorGroup.GetDefaultSensorDeviceIndex
---

# IMFSensorGroup::GetDefaultSensorDeviceIndex


## -description

Retrieves the index of the default device in the sensor group.

## -parameters

### -param pdwIndex [out]

If the call succeeds, <i>pdwIndex</i> receives the index of the default device.

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
The <i>pdwIndex</i> parameter is null.

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

The term "device" in this context could refer to a physical device, a custom media source, or a frame provider.

If this <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensorgroup-setdefaultsensordeviceindex">SetDefaultSensorDevice</a> has not been called, the first device in the Sensor Group (i.e. index 0) will be returned.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>