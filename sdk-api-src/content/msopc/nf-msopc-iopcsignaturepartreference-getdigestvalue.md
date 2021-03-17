---
UID: NF:msopc.IOpcSignaturePartReference.GetDigestValue
title: IOpcSignaturePartReference::GetDigestValue (msopc.h)
description: Gets the digest value that is calculated for part content of the referenced part when the part is signed.
helpviewer_keywords: ["GetDigestValue","GetDigestValue method [Open Packaging Conventions]","GetDigestValue method [Open Packaging Conventions]","IOpcSignaturePartReference interface","IOpcSignaturePartReference interface [Open Packaging Conventions]","GetDigestValue method","IOpcSignaturePartReference.GetDigestValue","IOpcSignaturePartReference::GetDigestValue","msopc/IOpcSignaturePartReference::GetDigestValue","opc.iopcsignaturepartreference_getdigestvalue"]
old-location: opc\iopcsignaturepartreference_getdigestvalue.htm
tech.root: OPC
ms.assetid: 43ae8891-34fb-46cf-8b61-f7d1bd67a2d2
ms.date: 12/05/2018
ms.keywords: GetDigestValue, GetDigestValue method [Open Packaging Conventions], GetDigestValue method [Open Packaging Conventions],IOpcSignaturePartReference interface, IOpcSignaturePartReference interface [Open Packaging Conventions],GetDigestValue method, IOpcSignaturePartReference.GetDigestValue, IOpcSignaturePartReference::GetDigestValue, msopc/IOpcSignaturePartReference::GetDigestValue, opc.iopcsignaturepartreference_getdigestvalue
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
 - IOpcSignaturePartReference::GetDigestValue
 - msopc/IOpcSignaturePartReference::GetDigestValue
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
 - IOpcSignaturePartReference.GetDigestValue
---

# IOpcSignaturePartReference::GetDigestValue


## -description

Gets the digest value that is calculated for part content of the referenced part when  the part is signed.

## -parameters

### -param digestValue [out]

A pointer to a buffer that contains the digest value that is calculated using the specified digest method; the method is  applied to part content of the referenced part when the part is signed.

### -param count [out]

The size of the <i>digestValue</i> buffer.

If the referenced part has not been signed yet, <i>count</i> is 0.

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
 At least one of the <i>digestValue</i>, and <i>count</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the buffer returned in <i>digestValue</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>