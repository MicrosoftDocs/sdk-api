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

# IAmsiStream::GetAttribute


## -description


Returns a requested attribute from the stream.


## -parameters




### -param attribute [in]

Specifies the type of attribute to be returned. See Remarks.


### -param dataSize [in]

The size of the output buffer, <i>data</i>, in bytes.


### -param data [out]

Buffer to receive the requested attribute. <i>data</i> must be set to its size in bytes.


### -param retData [out]

The number of bytes returned in <i>data</i>. If this method returns <b>E_NOT_SUFFICIENT_BUFFER</b>, <i>retData</i> contains the number of bytes required.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The attribute is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer, as indicated by <i>data</i>, is not large enough. <i>retData</i> contains the number of bytes required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>
 




## -remarks



Depending on the attribute requested in <i>attribute</i>, the following data should be copied to <i>data</i>:

<table>
<tr>
<th><i>attribute</i></th>
<th><i>data</i></th>
</tr>
<tr>
<td><b>AMSI_ATTRIBUTE_APP_NAME</b></td>
<td>The name, version, or GUID string of the calling application, copied from a <b>LPWSTR</b>.</td>
</tr>
<tr>
<td><b>AMSI_ATTRIBUTE_CONTENT_NAME</b></td>
<td>The filename, URL, unique script ID, or similar of the content, copied from a <b>LPWSTR</b>.</td>
</tr>
<tr>
<td><b>AMSI_ATTRIBUTE_CONTENT_SIZE</b></td>
<td>The  size of the input, as a <b>ULONGLONG</b>.</td>
</tr>
<tr>
<td><b>AMSI_ATTRIBUTE_CONTENT_ADDRESS</b></td>
<td>The  memory address if the content is fully loaded into memory.</td>
</tr>
<tr>
<td><b>AMSI_ATTRIBUTE_SESSION</b></td>
<td>Session is used to associate different scan calls, such as if the contents
    to be scanned belong to the same original script. Return <b>nullptr</b> if the content
    is self-contained.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/19DD293C-71FF-4E40-A2B7-12B4A2D00DBD">AMSI_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/409CE6BF-57A5-454E-91F9-3D66FE7E323F">IAmsiStream</a>
 

 

