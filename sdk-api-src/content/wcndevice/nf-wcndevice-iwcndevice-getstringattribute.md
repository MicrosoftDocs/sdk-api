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

# IWCNDevice::GetStringAttribute


## -description


The <b>IWCNDevice::GetStringAttribute</b> method gets a cached attribute  from the device as a string.


## -parameters




### -param AttributeType [in]

A <b>WCN_ATTRIBUTE_TYPE</b> value that represents a specific attribute value (for example,   <b>WCN_PASSWORD_TYPE</b>). If the attribute is not natively a string data type (for example, <b>WCN_TYPE_VERSION</b> is natively an integer, and <b>WNC_TYPE_SSID</b> is natively a blob), this function will fail with <b>HRESULT_FROM_WIN32(ERROR_INVALID_DATATYPE)</b>.


### -param cchMaxString [in]

The size of the buffer <i>wszString</i>, in characters.


### -param wszString [out]

A user-allocated buffer that,  on successful return, contains a <b>NULL</b>-terminated string value of the vendor extension.


## -returns



...

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
The attribute was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The attribute specified is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>wszString</i> is not large enough to contain the returned attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATATYPE)</b></dt>
</dl>
</td>
<td width="60%">
This attribute cannot be expressed as a string. For example, if it is an integer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>



<b>WCN_ATTRIBUTE_TYPE</b>
 

 

