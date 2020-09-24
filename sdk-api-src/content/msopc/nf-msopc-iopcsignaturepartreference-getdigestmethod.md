---
UID: NF:msopc.IOpcSignaturePartReference.GetDigestMethod
title: IOpcSignaturePartReference::GetDigestMethod (msopc.h)
description: Gets the digest method to use on part content of the referenced part when the part is signed.
helpviewer_keywords: ["GetDigestMethod","GetDigestMethod method [Open Packaging Conventions]","GetDigestMethod method [Open Packaging Conventions]","IOpcSignaturePartReference interface","IOpcSignaturePartReference interface [Open Packaging Conventions]","GetDigestMethod method","IOpcSignaturePartReference.GetDigestMethod","IOpcSignaturePartReference::GetDigestMethod","msopc/IOpcSignaturePartReference::GetDigestMethod","opc.iopcsignaturepartreference_getdigestmethod"]
old-location: opc\iopcsignaturepartreference_getdigestmethod.htm
tech.root: OPC
ms.assetid: 750aec1a-92b4-4c70-8c17-c15c9536bc41
ms.date: 12/05/2018
ms.keywords: GetDigestMethod, GetDigestMethod method [Open Packaging Conventions], GetDigestMethod method [Open Packaging Conventions],IOpcSignaturePartReference interface, IOpcSignaturePartReference interface [Open Packaging Conventions],GetDigestMethod method, IOpcSignaturePartReference.GetDigestMethod, IOpcSignaturePartReference::GetDigestMethod, msopc/IOpcSignaturePartReference::GetDigestMethod, opc.iopcsignaturepartreference_getdigestmethod
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
 - IOpcSignaturePartReference::GetDigestMethod
 - msopc/IOpcSignaturePartReference::GetDigestMethod
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
 - IOpcSignaturePartReference.GetDigestMethod
---

# IOpcSignaturePartReference::GetDigestMethod


## -description

Gets the digest method to use on part content of the referenced part when the part is signed.

## -parameters

### -param digestMethod [out, retval]

The digest method to use on part content of the referenced part when the part is signed.

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
The <i>digestMethod</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>digestMethod</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.


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