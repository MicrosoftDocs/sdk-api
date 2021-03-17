---
UID: NF:amsi.IAmsiStream.GetAttribute
title: IAmsiStream::GetAttribute (amsi.h)
description: Returns a requested attribute from the stream.
helpviewer_keywords: ["GetAttribute","GetAttribute method [Antimalware Scan Interface]","GetAttribute method [Antimalware Scan Interface]","IAmsiStream interface","IAmsiStream interface [Antimalware Scan Interface]","GetAttribute method","IAmsiStream.GetAttribute","IAmsiStream::GetAttribute","amsi.iamsistream_getattribute","amsi/IAmsiStream::GetAttribute"]
old-location: amsi\iamsistream_getattribute.htm
tech.root: AMSI
ms.assetid: 7AD74D85-1A1E-4AFD-91C1-670AC7280285
ms.date: 12/05/2018
ms.keywords: GetAttribute, GetAttribute method [Antimalware Scan Interface], GetAttribute method [Antimalware Scan Interface],IAmsiStream interface, IAmsiStream interface [Antimalware Scan Interface],GetAttribute method, IAmsiStream.GetAttribute, IAmsiStream::GetAttribute, amsi.iamsistream_getattribute, amsi/IAmsiStream::GetAttribute
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IAmsiStream::GetAttribute
 - amsi/IAmsiStream::GetAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amsi.h
api_name:
 - IAmsiStream.GetAttribute
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

<a href="/windows/desktop/api/amsi/ne-amsi-amsi_attribute">AMSI_ATTRIBUTE</a>



<a href="/windows/desktop/api/amsi/nn-amsi-iamsistream">IAmsiStream</a>