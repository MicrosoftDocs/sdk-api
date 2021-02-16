---
UID: NF:msopc.IOpcSignatureReference.GetDigestMethod
title: IOpcSignatureReference::GetDigestMethod (msopc.h)
description: Gets the digest method to use on the referenced XML element, when the element is signed.
helpviewer_keywords: ["GetDigestMethod","GetDigestMethod method [Open Packaging Conventions]","GetDigestMethod method [Open Packaging Conventions]","IOpcSignatureReference interface","IOpcSignatureReference interface [Open Packaging Conventions]","GetDigestMethod method","IOpcSignatureReference.GetDigestMethod","IOpcSignatureReference::GetDigestMethod","msopc/IOpcSignatureReference::GetDigestMethod","opc.iopcsignaturereference_getdigestmethod"]
old-location: opc\iopcsignaturereference_getdigestmethod.htm
tech.root: OPC
ms.assetid: 438adeba-bf5f-4f87-ab4c-c370e58565ce
ms.date: 12/05/2018
ms.keywords: GetDigestMethod, GetDigestMethod method [Open Packaging Conventions], GetDigestMethod method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetDigestMethod method, IOpcSignatureReference.GetDigestMethod, IOpcSignatureReference::GetDigestMethod, msopc/IOpcSignatureReference::GetDigestMethod, opc.iopcsignaturereference_getdigestmethod
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
 - IOpcSignatureReference::GetDigestMethod
 - msopc/IOpcSignatureReference::GetDigestMethod
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
 - IOpcSignatureReference.GetDigestMethod
---

# IOpcSignatureReference::GetDigestMethod


## -description

Gets the digest method to use on the referenced XML element, when the element is signed.

## -parameters

### -param digestMethod [out, retval]

The digest method to use on the referenced XML element.

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



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>