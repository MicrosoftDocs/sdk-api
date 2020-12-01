---
UID: NF:mfidl.IMFSensorDevice.GetStreamAttributesCount
title: IMFSensorDevice::GetStreamAttributesCount (mfidl.h)
description: Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.
helpviewer_keywords: ["GetStreamAttributesCount","GetStreamAttributesCount method [Media Foundation]","GetStreamAttributesCount method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetStreamAttributesCount method","IMFSensorDevice.GetStreamAttributesCount","IMFSensorDevice::GetStreamAttributesCount","mf.imfsensordevice_getstreamattributescount","mfidl/IMFSensorDevice::GetStreamAttributesCount"]
old-location: mf\imfsensordevice_getstreamattributescount.htm
tech.root: mf
ms.assetid: C6A0C4E6-7939-42C1-A499-7C92D83CB418
ms.date: 12/05/2018
ms.keywords: GetStreamAttributesCount, GetStreamAttributesCount method [Media Foundation], GetStreamAttributesCount method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetStreamAttributesCount method, IMFSensorDevice.GetStreamAttributesCount, IMFSensorDevice::GetStreamAttributesCount, mf.imfsensordevice_getstreamattributescount, mfidl/IMFSensorDevice::GetStreamAttributesCount
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
 - IMFSensorDevice::GetStreamAttributesCount
 - mfidl/IMFSensorDevice::GetStreamAttributesCount
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
 - IMFSensorDevice.GetStreamAttributesCount
---

# IMFSensorDevice::GetStreamAttributesCount


## -description

Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.

## -parameters

### -param eType [in]

A member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensorstreamtype">MFSensorStreamType</a> enumeration specifying whether the attribute store count is being requested for an input or output stream.

### -param pdwCount [out]

The number of stream attributes available for this sensor device.

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
The <i>pdwCount</i> parameter is null.

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

The caller can use the number of stream attributes to indicate the number of streams provided by the sensor device.  

<div class="alert"><b>Note</b>  Depending on the sharing mode in which the sensor device was activated, not all streams may be present during runtime.  Streams marked as shared, i.e. with the <a href="/windows/desktop/medfound/mf-devicestream-frameserver-shared">MF_DEVICESTREAM_FRAMESERVER_SHARED</a> attribute set to non-zero value, and streams with pins with the category <b>PINNAME_VIDEO_PREVIEW</b> will be present in devices that are set to used shared mode. Put a device in shared mode by passing <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensordevicemode">MFSensorDeviceMode_Shared</a> into <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-setsensordevicemode">SetSensorDeviceMode</a>.
If no streams are marked as shared and no preview stream is available, the first capture stream, with the category <b>PINNAME_VIDEO_CAPTURE</b>,  will be shared.
</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>