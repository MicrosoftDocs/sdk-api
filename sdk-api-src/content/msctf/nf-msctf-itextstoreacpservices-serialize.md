---
UID: NF:msctf.ITextStoreACPServices.Serialize
title: ITextStoreACPServices::Serialize (msctf.h)
description: ITextStoreACPServices::Serialize method
helpviewer_keywords: ["ITextStoreACPServices interface [Text Services Framework]","Serialize method","ITextStoreACPServices.Serialize","ITextStoreACPServices::Serialize","Serialize","Serialize method [Text Services Framework]","Serialize method [Text Services Framework]","ITextStoreACPServices interface","_tsf_itextstoreacpservices_serialize_ref","msctf/ITextStoreACPServices::Serialize","tsf.itextstoreacpservices_serialize"]
old-location: tsf\itextstoreacpservices_serialize.htm
tech.root: TSF
ms.assetid: 14be52d1-4f8c-4deb-aa92-470c3608c841
ms.date: 12/05/2018
ms.keywords: ITextStoreACPServices interface [Text Services Framework],Serialize method, ITextStoreACPServices.Serialize, ITextStoreACPServices::Serialize, Serialize, Serialize method [Text Services Framework], Serialize method [Text Services Framework],ITextStoreACPServices interface, _tsf_itextstoreacpservices_serialize_ref, msctf/ITextStoreACPServices::Serialize, tsf.itextstoreacpservices_serialize
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreACPServices::Serialize
 - msctf/ITextStoreACPServices::Serialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPServices.Serialize
---

# ITextStoreACPServices::Serialize


## -description

Obtains a property from a range of text and writes the property data into a stream object.

## -parameters

### -param pProp [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a> interface that identifies the property to serialize.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that identifies the range that the property is obtained from.

### -param pHdr [out]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that receives the header data for the property.

### -param pStream [in]

Pointer to an <b>IStream</b> object that the TSF manager will write the property data to.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property cannot be serialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

The property header data placed in <i>pHdr</i> is generic to all properties and must be preserved with the data written into <i>pStream</i>. This same data pair must be passed to <a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize</a> to restore the property data.

An application can save all of the properties for the entire document by performing the following steps.

<ul>
<li>Enumerate all properties using <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties">ITfContext::EnumProperties</a>.</li>
<li>Within each property, enumerate the ranges using <a href="/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges">ITfReadOnlyProperty::EnumRanges</a>.</li>
<li>Pass the current property and range to <b>ITextStoreACPServices::Serialize</b>.</li>
<li>Write the data placed in <i>pHdr</i> to the file.</li>
<li>Write the data added to <i>pStream</i> to the file.</li>
</ul>
When calling this method, the application must be able to grant a synchronous read-only lock.

## -see-also

[ITextStoreACPServices interface](nn-msctf-itextstoreacpservices.md), [ITextStoreACPServices::Unserialize](nf-msctf-itextstoreacpservices-unserialize.md), [ITfContext::EnumProperties](nf-msctf-itfcontext-enumproperties.md), [ITfProperty interface](nn-msctf-itfproperty.md), [ITfRange interface](nn-msctf-itfrange.md), [ITfReadOnlyProperty::EnumRanges](nf-msctf-itfreadonlyproperty-enumranges.md), [TF_PERSISTENT_PROPERTY_HEADER_ACP structure](ns-msctf-tf_persistent_property_header_acp.md)