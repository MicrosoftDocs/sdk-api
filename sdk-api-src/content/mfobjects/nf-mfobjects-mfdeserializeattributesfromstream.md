---
UID: NF:mfobjects.MFDeserializeAttributesFromStream
title: MFDeserializeAttributesFromStream function (mfobjects.h)
description: Loads attributes from a stream into an attribute store.
helpviewer_keywords: ["MFDeserializeAttributesFromStream","MFDeserializeAttributesFromStream function [Media Foundation]","cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a","mf.mfdeserializeattributesfromstream","mfobjects/MFDeserializeAttributesFromStream"]
old-location: mf\mfdeserializeattributesfromstream.htm
tech.root: mf
ms.assetid: cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a
ms.date: 12/05/2018
ms.keywords: MFDeserializeAttributesFromStream, MFDeserializeAttributesFromStream function [Media Foundation], cc0bccfd-7e67-4e55-9d3e-ebcd91b94a3a, mf.mfdeserializeattributesfromstream, mfobjects/MFDeserializeAttributesFromStream
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFDeserializeAttributesFromStream
 - mfobjects/MFDeserializeAttributesFromStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFDeserializeAttributesFromStream
---

# MFDeserializeAttributesFromStream function


## -description

Loads attributes from a stream into an attribute store.

## -parameters

### -param pAttr

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param dwOptions

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_serialize_options">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a> enumeration.

### -param pStm

Pointer to the <b>IStream</b> interface of the stream from which to read the attributes.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -remarks

Use this function to deserialize an attribute store that was serialized with the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream">MFSerializeAttributesToStream</a> function.

If <i>dwOptions</i> contains the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function deserializes <b>IUnknown</b> pointers from the stream, as follows:

<ul>
<li>
If the <b>IStream</b> pointer exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream">IMFObjectReferenceStream</a> interface (through <b>QueryInterface</b>), the function calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfobjectreferencestream-loadreference">IMFObjectReferenceStream::LoadReference</a> to deserialize each pointer.

</li>
<li>
Otherwise, the function calls <b>CoUnmarshalInterface</b> to deserialize a proxy for the object.

</li>
</ul>
This function deletes any attributes that were previously stored in <i>pAttr</i>.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_serialize_options">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>