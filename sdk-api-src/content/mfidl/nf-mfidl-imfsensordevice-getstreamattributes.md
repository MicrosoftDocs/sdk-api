---
UID: NF:mfidl.IMFSensorDevice.GetStreamAttributes
title: IMFSensorDevice::GetStreamAttributes (mfidl.h)
description: Gets the stream attribute store with the specified index.
helpviewer_keywords: ["GetStreamAttributes","GetStreamAttributes method [Media Foundation]","GetStreamAttributes method [Media Foundation]","IMFSensorDevice interface","IMFSensorDevice interface [Media Foundation]","GetStreamAttributes method","IMFSensorDevice.GetStreamAttributes","IMFSensorDevice::GetStreamAttributes","mf.imfsensordevice_getstreamattributes","mfidl/IMFSensorDevice::GetStreamAttributes"]
old-location: mf\imfsensordevice_getstreamattributes.htm
tech.root: mf
ms.assetid: DDBEB335-E6E3-4185-B7EF-90FABA9CDCE5
ms.date: 12/05/2018
ms.keywords: GetStreamAttributes, GetStreamAttributes method [Media Foundation], GetStreamAttributes method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetStreamAttributes method, IMFSensorDevice.GetStreamAttributes, IMFSensorDevice::GetStreamAttributes, mf.imfsensordevice_getstreamattributes, mfidl/IMFSensorDevice::GetStreamAttributes
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
 - IMFSensorDevice::GetStreamAttributes
 - mfidl/IMFSensorDevice::GetStreamAttributes
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
 - IMFSensorDevice.GetStreamAttributes
---

# IMFSensorDevice::GetStreamAttributes


## -description

Gets the stream attribute store with the specified index.

## -parameters

### -param eType [in]

A member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mfsensorstreamtype">MFSensorStreamType</a> enumeration specifying whether the attribute store is being requested for an input or output stream.

### -param dwIndex [in]

The 0-based index of the stream to be retrieved.  The index must be between 0 and the value returned by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsensordevice-getstreamattributescount">GetStreamAttributesCount</a> - 1.

### -param ppAttributes [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface representing a copy internal attribute store of the stream.

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

The object returned is a copy of the internal attribute store and so changes made to the returned attributes have no effect on the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice">IMFSensorDevice</a>