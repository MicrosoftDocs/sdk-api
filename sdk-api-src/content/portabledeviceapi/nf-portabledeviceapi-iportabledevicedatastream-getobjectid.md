---
UID: NF:portabledeviceapi.IPortableDeviceDataStream.GetObjectID
title: IPortableDeviceDataStream::GetObjectID (portabledeviceapi.h)
description: The GetObjectID method retrieves the object ID of the resource that was written to the device. This method is only valid after calling IStream::Commit on the data stream.
helpviewer_keywords: ["GetObjectID","GetObjectID method [Windows Portable Devices SDK]","GetObjectID method [Windows Portable Devices SDK]","IPortableDeviceDataStream interface","IPortableDeviceDataStream interface [Windows Portable Devices SDK]","GetObjectID method","IPortableDeviceDataStream.GetObjectID","IPortableDeviceDataStream::GetObjectID","IPortableDeviceDataStreamGetObjectID","portabledeviceapi/IPortableDeviceDataStream::GetObjectID","wpdsdk.iportabledevicedatastream_getobjectid"]
old-location: wpdsdk\iportabledevicedatastream_getobjectid.htm
tech.root: wpdsdk
ms.assetid: bd506e52-723d-4a3c-b73e-425700ccd3ec
ms.date: 12/05/2018
ms.keywords: GetObjectID, GetObjectID method [Windows Portable Devices SDK], GetObjectID method [Windows Portable Devices SDK],IPortableDeviceDataStream interface, IPortableDeviceDataStream interface [Windows Portable Devices SDK],GetObjectID method, IPortableDeviceDataStream.GetObjectID, IPortableDeviceDataStream::GetObjectID, IPortableDeviceDataStreamGetObjectID, portabledeviceapi/IPortableDeviceDataStream::GetObjectID, wpdsdk.iportabledevicedatastream_getobjectid
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceDataStream::GetObjectID
 - portabledeviceapi/IPortableDeviceDataStream::GetObjectID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceDataStream.GetObjectID
---

# IPortableDeviceDataStream::GetObjectID


## -description

The <b>GetObjectID</b> method retrieves the object ID of the resource that was written to the device. This method is only valid after calling <b>IStream::Commit</b> on the data stream.

## -parameters

### -param ppszObjectID [out]

The ID of the object just transferred to the device.

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
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>

## -remarks

An object ID is created after the object is created on the device. Therefore, a new object that is created by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a> will not have an ID assigned until the application calls <b>Commit</b> on the data transfer stream.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicedatastream">IPortableDeviceDataStream Interface</a>