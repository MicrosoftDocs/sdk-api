---
UID: NF:mfobjects.MFSerializeAttributesToStream
title: MFSerializeAttributesToStream function (mfobjects.h)
description: Writes the contents of an attribute store to a stream.
helpviewer_keywords: ["MFSerializeAttributesToStream","MFSerializeAttributesToStream function [Media Foundation]","b8bc88e5-19ae-46b3-aa78-a00afee1f481","mf.mfserializeattributestostream","mfobjects/MFSerializeAttributesToStream"]
old-location: mf\mfserializeattributestostream.htm
tech.root: mf
ms.assetid: b8bc88e5-19ae-46b3-aa78-a00afee1f481
ms.date: 12/05/2018
ms.keywords: MFSerializeAttributesToStream, MFSerializeAttributesToStream function [Media Foundation], b8bc88e5-19ae-46b3-aa78-a00afee1f481, mf.mfserializeattributestostream, mfobjects/MFSerializeAttributesToStream
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
 - MFSerializeAttributesToStream
 - mfobjects/MFSerializeAttributesToStream
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
 - MFSerializeAttributesToStream
---

# MFSerializeAttributesToStream function


## -description

Writes the contents of an attribute store to a stream.

## -parameters

### -param pAttr

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param dwOptions

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_serialize_options">MF_ATTRIBUTE_SERIALIZE_OPTIONS</a> enumeration.

### -param pStm

Pointer to the <b>IStream</b> interface of the stream where the attributes are saved.

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

If <i>dwOptions</i> contains the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function serializes <b>IUnknown</b> pointers in the attribute store, as follows:

<ul>
<li>
If the <b>IStream</b> pointer exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream">IMFObjectReferenceStream</a> interface (through <b>QueryInterface</b>), the function calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfobjectreferencestream-savereference">IMFObjectReferenceStream::SaveReference</a> to serialize each pointer.

</li>
<li>
Otherwise, the function calls <b>CoMarshalInterface</b> to serialize a proxy for the object.

</li>
</ul>
If <i>dwOptions</i> does not include the MF_ATTRIBUTE_SERIALIZE_UNKNOWN_BYREF flag, the function skips <b>IUnknown</b> pointers in the attribute store.

To load the attributes from the stream, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream">MFDeserializeAttributesFromStream</a>.

The main purpose of this function is to marshal attributes across process boundaries.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>