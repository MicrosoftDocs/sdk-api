---
UID: NF:wcndevice.IWCNDevice.GetStringAttribute
title: IWCNDevice::GetStringAttribute
author: windows-sdk-content
description: The IWCNDevice::GetStringAttribute method gets a cached attribute from the device as a string.
old-location: wcn\iwcndevice_getstringattribute.htm
old-project: wcn
ms.assetid: 4ef065be-0046-4ce6-8f81-417a4c8a550a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetStringAttribute, GetStringAttribute method [Windows Connect Now], GetStringAttribute method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetStringAttribute method, IWCNDevice.GetStringAttribute, IWCNDevice::GetStringAttribute, wcn.iwcndevice_getstringattribute, wcndevice/IWCNDevice::GetStringAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcndevice.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_SESSION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.GetStringAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

