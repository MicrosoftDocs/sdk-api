---
UID: NF:msopc.IOpcSignatureReference.GetType
title: IOpcSignatureReference::GetType (msopc.h)
description: Gets a string that indicates the type of the referenced XML element.
helpviewer_keywords: ["GetType","GetType method [Open Packaging Conventions]","GetType method [Open Packaging Conventions]","IOpcSignatureReference interface","IOpcSignatureReference interface [Open Packaging Conventions]","GetType method","IOpcSignatureReference.GetType","IOpcSignatureReference::GetType","msopc/IOpcSignatureReference::GetType","opc.iopcsignaturereference_gettype"]
old-location: opc\iopcsignaturereference_gettype.htm
tech.root: OPC
ms.assetid: 7402f031-b06c-4fc6-bb54-ad9fc28600b3
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Open Packaging Conventions], GetType method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetType method, IOpcSignatureReference.GetType, IOpcSignatureReference::GetType, msopc/IOpcSignatureReference::GetType, opc.iopcsignaturereference_gettype
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
 - IOpcSignatureReference::GetType
 - msopc/IOpcSignatureReference::GetType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureReference.GetType
---

# IOpcSignatureReference::GetType


## -description

Gets a string that indicates the type of the referenced XML  element.

## -parameters

### -param type [out, retval]

A string that indicates the type of the referenced XML  element.

If the type  is not set, the <i>type</i> parameter will be the empty string "".

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>type</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>type</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

Providing a type for the referenced XML  element is optional. If used, the type of the referenced element is serialized in the signature markup as the optional <b>Type</b> attribute  value of a <b>Reference</b> element. 

The caller can use the type of the referenced element to indicate whether the element  is an <b>Object</b>, <b>SignatureProperty</b>, or <b>Manifest</b> element. This identification can aid the caller in processing the reference.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>