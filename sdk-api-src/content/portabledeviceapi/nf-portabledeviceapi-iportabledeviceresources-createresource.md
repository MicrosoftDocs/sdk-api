---
UID: NF:portabledeviceapi.IPortableDeviceResources.CreateResource
title: IPortableDeviceResources::CreateResource (portabledeviceapi.h)
description: The CreateResource method creates a resource.
helpviewer_keywords: ["CreateResource","CreateResource method [Windows Portable Devices SDK]","CreateResource method [Windows Portable Devices SDK]","IPortableDeviceResources interface","IPortableDeviceResources interface [Windows Portable Devices SDK]","CreateResource method","IPortableDeviceResources.CreateResource","IPortableDeviceResources::CreateResource","IPortableDeviceResourcesCreateResource","portabledeviceapi/IPortableDeviceResources::CreateResource","wpdsdk.iportabledeviceresources_createresource"]
old-location: wpdsdk\iportabledeviceresources_createresource.htm
tech.root: wpdsdk
ms.assetid: 1daaa2cd-d3a7-44ea-b17d-717875ff748d
ms.date: 12/05/2018
ms.keywords: CreateResource, CreateResource method [Windows Portable Devices SDK], CreateResource method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],CreateResource method, IPortableDeviceResources.CreateResource, IPortableDeviceResources::CreateResource, IPortableDeviceResourcesCreateResource, portabledeviceapi/IPortableDeviceResources::CreateResource, wpdsdk.iportabledeviceresources_createresource
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
 - IPortableDeviceResources::CreateResource
 - portabledeviceapi/IPortableDeviceResources::CreateResource
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
 - IPortableDeviceResources.CreateResource
---

# IPortableDeviceResources::CreateResource


## -description

The <b>CreateResource</b> method creates a resource.

## -parameters

### -param pResourceAttributes [in]

Pointer to the following object parameter attributes.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>WPD_OBJECT_NAME</td>
<td>The object name.</td>
</tr>
<tr>
<td>WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE</td>
<td>The total size of the resource data stream.</td>
</tr>
<tr>
<td>WPD_RESOURCE_ATTRIBUTE_FORMAT</td>
<td>The format of the resource data stream.</td>
</tr>
<tr>
<td>WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY</td>
<td>The resource key.</td>
</tr>
</table>

### -param ppData [out]

Pointer to a stream into which the caller can write resource data.

### -param pdwOptimalWriteBufferSize [out]

Pointer to a value that specifies the optimal buffer size when writing to the stream. This parameter is optional.

### -param ppszCookie [out]

Pointer to a cookie that identifies the resource creation request. This parameter is optional.

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
At least one of the arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -remarks

When an application calls this method, it must specify the resource attributes and it must write the required data to the stream that this method returns.

A resource is not created when the method returns; it is created when the application commits the data by calling the <b>Commit</b> method on the stream at which <i>ppData</i> points.

To cancel the data transfer to a resource, the application must call the <b>Revert</b> method on the stream at which <i>ppData</i> points. Once the transfer is canceled, the application must invoke <b>IUnknown::Release</b> to close the stream.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceresources">IPortableDeviceResources Interface</a>