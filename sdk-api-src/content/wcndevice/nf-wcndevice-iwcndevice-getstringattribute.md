---
UID: NF:wcndevice.IWCNDevice.GetStringAttribute
title: IWCNDevice::GetStringAttribute (wcndevice.h)
description: The IWCNDevice::GetStringAttribute method gets a cached attribute from the device as a string.
helpviewer_keywords: ["GetStringAttribute","GetStringAttribute method [Windows Connect Now]","GetStringAttribute method [Windows Connect Now]","IWCNDevice interface","IWCNDevice interface [Windows Connect Now]","GetStringAttribute method","IWCNDevice.GetStringAttribute","IWCNDevice::GetStringAttribute","wcn.iwcndevice_getstringattribute","wcndevice/IWCNDevice::GetStringAttribute"]
old-location: wcn\iwcndevice_getstringattribute.htm
tech.root: wcn
ms.assetid: 4ef065be-0046-4ce6-8f81-417a4c8a550a
ms.date: 12/05/2018
ms.keywords: GetStringAttribute, GetStringAttribute method [Windows Connect Now], GetStringAttribute method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetStringAttribute method, IWCNDevice.GetStringAttribute, IWCNDevice::GetStringAttribute, wcn.iwcndevice_getstringattribute, wcndevice/IWCNDevice::GetStringAttribute
req.header: wcndevice.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWCNDevice::GetStringAttribute
 - wcndevice/IWCNDevice::GetStringAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.GetStringAttribute
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

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>



<b>WCN_ATTRIBUTE_TYPE</b>