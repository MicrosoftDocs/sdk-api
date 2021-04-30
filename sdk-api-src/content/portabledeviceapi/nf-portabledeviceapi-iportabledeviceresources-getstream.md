---
UID: NF:portabledeviceapi.IPortableDeviceResources.GetStream
title: IPortableDeviceResources::GetStream (portabledeviceapi.h)
description: The GetStream method gets an IStream interface with which to read or write the content data in an object on a device. The retrieved interface enables you to read from or write to the object data.
helpviewer_keywords: ["GetStream","GetStream method [Windows Portable Devices SDK]","GetStream method [Windows Portable Devices SDK]","IPortableDeviceResources interface","IPortableDeviceResources interface [Windows Portable Devices SDK]","GetStream method","IPortableDeviceResources.GetStream","IPortableDeviceResources::GetStream","IPortableDeviceResourcesGetStream","portabledeviceapi/IPortableDeviceResources::GetStream","wpdsdk.iportabledeviceresources_getstream"]
old-location: wpdsdk\iportabledeviceresources_getstream.htm
tech.root: wpdsdk
ms.assetid: d5c9a85a-59fa-4b7b-acc7-d450ecd10593
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [Windows Portable Devices SDK], GetStream method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],GetStream method, IPortableDeviceResources.GetStream, IPortableDeviceResources::GetStream, IPortableDeviceResourcesGetStream, portabledeviceapi/IPortableDeviceResources::GetStream, wpdsdk.iportabledeviceresources_getstream
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
 - IPortableDeviceResources::GetStream
 - portabledeviceapi/IPortableDeviceResources::GetStream
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
 - IPortableDeviceResources.GetStream
---

# IPortableDeviceResources::GetStream


## -description

The <b>GetStream</b> method gets an <b>IStream</b> interface with which to read or write the content data in an object on a device. The retrieved interface enables you to read from or write to the object data.

## -parameters

### -param pszObjectID [in]

Pointer to a null-terminated string that contains the object ID of the object.

### -param Key [in]

A <b>REFPROPERTYKEY</b> that specifies which resource to read. You can retrieve the keys of all the object's resources by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceresources-getsupportedresources">GetSupportedResources</a>.

### -param dwMode [in]

One of the following access modes:

<ul>
<li>STGM_READ (Read-only access.)</li>
<li>STGM_WRITE (Write-only access.)</li>
<li>STGM_READWRITE (Read/write access.)</li>
</ul>

### -param pdwOptimalBufferSize [in, out]

An optional pointer to a <b>DWORD</b> that specifies an estimate of the best buffer size to use when reading or writing data by using <i>ppStream</i>. A driver is required to support this value.

### -param ppStream [out]

Pointer to an <b>IStream</b> interface pointer. This interface is used to read and write data to the object. The caller must release this interface when it is done with it.

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
At least one of the required pointer arguments was <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The retrieved stream cannot read the contents of a folder recursively. To copy all the resources in an object, specify <b>WPD_RESOURCE_DEFAULT</b> for <i>Key</i>.

If the object does not support resources, this method will return an error, and <i>ppStream</i> will be <b>NULL</b>.

Applications should use the buffer size returned by <i>pdwOptimalBufferSize</i> when allocating the buffer for read or write operations.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceresources">IPortableDeviceResources Interface</a>