---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




<a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources Interface</a>
 

 

