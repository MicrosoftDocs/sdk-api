---
UID: NF:mfidl.MFSerializePresentationDescriptor
title: MFSerializePresentationDescriptor function (mfidl.h)
description: Serializes a presentation descriptor to a byte array.
helpviewer_keywords: ["MFSerializePresentationDescriptor","MFSerializePresentationDescriptor function [Media Foundation]","f39a0dc8-438e-4723-94e4-a194a0a460e3","mf.mfserializepresentationdescriptor","mfidl/MFSerializePresentationDescriptor"]
old-location: mf\mfserializepresentationdescriptor.htm
tech.root: mf
ms.assetid: f39a0dc8-438e-4723-94e4-a194a0a460e3
ms.date: 12/05/2018
ms.keywords: MFSerializePresentationDescriptor, MFSerializePresentationDescriptor function [Media Foundation], f39a0dc8-438e-4723-94e4-a194a0a460e3, mf.mfserializepresentationdescriptor, mfidl/MFSerializePresentationDescriptor
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFSerializePresentationDescriptor
 - mfidl/MFSerializePresentationDescriptor
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
 - MFSerializePresentationDescriptor
---

# MFSerializePresentationDescriptor function


## -description

Serializes a presentation descriptor to a byte array.

## -parameters

### -param pPD

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor to serialize.

### -param pcbData

Receives the size of the <i>ppbData</i> array, in bytes.

### -param ppbData

Receives a pointer to an array of bytes containing the serialized presentation descriptor. The caller must free the memory for the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
The function succeeded.

</td>
</tr>
</table>

## -remarks

To deserialize the presentation descriptor, pass the byte array to the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfdeserializepresentationdescriptor">MFDeserializePresentationDescriptor</a> function.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>