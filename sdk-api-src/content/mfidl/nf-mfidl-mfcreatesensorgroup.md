---
UID: NF:mfidl.MFCreateSensorGroup
title: MFCreateSensorGroup function (mfidl.h)
description: Creates an instance of the IMFSensorGroup interface based on the provided symbolic link name.
helpviewer_keywords: ["MFCreateSensorGroup","MFCreateSensorGroup function [Media Foundation]","mf.mfcreatesensorgroup","mfidl/MFCreateSensorGroup"]
old-location: mf\mfcreatesensorgroup.htm
tech.root: mf
ms.assetid: A1DDA62D-D668-4292-9DFF-09B17A78A54E
ms.date: 12/05/2018
ms.keywords: MFCreateSensorGroup, MFCreateSensorGroup function [Media Foundation], mf.mfcreatesensorgroup, mfidl/MFCreateSensorGroup
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps \| UWP apps]
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
req.lib: mfsensorgroup.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSensorGroup
 - mfidl/MFCreateSensorGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - MFCreateSensorGroup
---

# MFCreateSensorGroup function


## -description

Creates an instance of the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> interface based on the provided symbolic link name.

## -parameters

### -param SensorGroupSymbolicLink

The symbolic link for the new <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>. This name can be obtained through device enumeration APIs such as <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources">MFEnumDeviceSources</a> or by getting the  <a href="/uwp/api/Windows.Devices.Enumeration.DeviceInformation">Id</a> property of the <a href="/uwp/api/Windows.Devices.Enumeration.DeviceInformation">DeviceInformation</a> class.

### -param ppSensorGroup [out]

The symbolic link for the new <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The supplied <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <b>LPCWSTR</b> is null.

</td>
</tr>
</table>

## -remarks

If the function succeeds, <i>ppSensorGroup</i> will point to a valid <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> object.  The caller must release this interface.

<div class="alert"><b>Note</b>  When this API is used with a <a href="/previous-versions/ff548567(v=vs.85)">KSCATEGORY_SENSOR_CAMERA</a> or <a href="/previous-versions/ff548567(v=vs.85)">KSCATEGORY_VIDEO_CAMERA</a> symbolic name, the resulting <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a> object will only contain one sensor device but behaves as a virtualized sensor group.  The caller  may use the resulting object in the same manner as a sensor group obtained from a <a href="/previous-versions/ff548567(v=vs.85)">KSCATEGORY_SENSOR_GROUP</a>.</div>
<div> </div>