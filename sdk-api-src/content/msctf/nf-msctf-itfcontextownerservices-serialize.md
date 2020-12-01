---
UID: NF:msctf.ITfContextOwnerServices.Serialize
title: ITfContextOwnerServices::Serialize (msctf.h)
description: The ITfContextOwnerServices::Serialize method obtains a property from a range of text and writes the property data into a stream object. This enables an application to store property data, for example, when writing the data to a file.
helpviewer_keywords: ["ITfContextOwnerServices interface [Text Services Framework]","Serialize method","ITfContextOwnerServices.Serialize","ITfContextOwnerServices::Serialize","Serialize","Serialize method [Text Services Framework]","Serialize method [Text Services Framework]","ITfContextOwnerServices interface","_tsf_itfcontextownerservices_serialize_ref","msctf/ITfContextOwnerServices::Serialize","tsf.itfcontextownerservices_serialize"]
old-location: tsf\itfcontextownerservices_serialize.htm
tech.root: TSF
ms.assetid: e67b6fa7-610d-426f-a290-36c0da4068f4
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],Serialize method, ITfContextOwnerServices.Serialize, ITfContextOwnerServices::Serialize, Serialize, Serialize method [Text Services Framework], Serialize method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_serialize_ref, msctf/ITfContextOwnerServices::Serialize, tsf.itfcontextownerservices_serialize
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
 - ITfContextOwnerServices::Serialize
 - msctf/ITfContextOwnerServices::Serialize
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
 - ITfContextOwnerServices.Serialize
---

# ITfContextOwnerServices::Serialize


## -description

The <b>ITfContextOwnerServices::Serialize</b> method obtains a property from a range of text and writes the property data into a stream object. This enables an application to store property data, for example, when writing the data to a file.

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

The property header data placed in <i>pHdr</i> is common to all properties and must be preserved with the data written into <i>pStream</i>. This same data pair must be passed to <a href="/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITfContextOwnerServices::Unserialize</a> to restore the property data.

An application can save all of the properties for the entire document by performing the following steps.

<ul>
<li>Enumerate all properties using <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties">ITfContext::EnumProperties</a>.</li>
<li>Within each property, enumerate the ranges using <a href="/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges">ITfReadOnlyProperty::EnumRanges</a>.</li>
<li>Pass the current property and range to this method.</li>
<li>Write the data placed in <i>pHdr</i> to the file.</li>
<li>Write the data added to <i>pStream</i> to the file.</li>
</ul>
When calling this method, the application must be able to grant a synchronous read-only lock.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownerservices">ITfContextOwnerServices</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>