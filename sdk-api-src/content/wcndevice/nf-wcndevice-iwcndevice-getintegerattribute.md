---
UID: NF:wcndevice.IWCNDevice.GetIntegerAttribute
title: IWCNDevice::GetIntegerAttribute (wcndevice.h)
description: The GetIntegerAttribute method gets a cached attribute from the device as an integer.
helpviewer_keywords: ["GetIntegerAttribute","GetIntegerAttribute method [Windows Connect Now]","GetIntegerAttribute method [Windows Connect Now]","IWCNDevice interface","IWCNDevice interface [Windows Connect Now]","GetIntegerAttribute method","IWCNDevice.GetIntegerAttribute","IWCNDevice::GetIntegerAttribute","wcn.iwcndevice_getintegerattribute","wcndevice/IWCNDevice::GetIntegerAttribute"]
old-location: wcn\iwcndevice_getintegerattribute.htm
tech.root: wcn
ms.assetid: 95ad3427-c8c9-4ac9-8c8e-c9bedf855a37
ms.date: 12/05/2018
ms.keywords: GetIntegerAttribute, GetIntegerAttribute method [Windows Connect Now], GetIntegerAttribute method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetIntegerAttribute method, IWCNDevice.GetIntegerAttribute, IWCNDevice::GetIntegerAttribute, wcn.iwcndevice_getintegerattribute, wcndevice/IWCNDevice::GetIntegerAttribute
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
 - IWCNDevice::GetIntegerAttribute
 - wcndevice/IWCNDevice::GetIntegerAttribute
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
 - IWCNDevice.GetIntegerAttribute
---

# IWCNDevice::GetIntegerAttribute


## -description

The <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getstringattribute">GetIntegerAttribute</a> method gets a cached attribute  from the device as an integer.

## -parameters

### -param AttributeType [in]

A <b>WCN_ATTRIBUTE_TYPE</b> value  that represents a specific attribute value (for example, <b>WCN_PASSWORD_TYPE</b>).

### -param puInteger [out]

Pointer to an unsigned-integer that represents the retrieved attribute value.

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
The buffer specified by <i>pbBuffer</i> is not large enough to contain the returned attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATATYPE)</b></dt>
</dl>
</td>
<td width="60%">
This attribute cannot be expressed as an integer. For example, if it is a string.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>



<b>WCN_ATTRIBUTE_TYPE</b>