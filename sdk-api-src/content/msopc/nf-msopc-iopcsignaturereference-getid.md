---
UID: NF:msopc.IOpcSignatureReference.GetId
title: IOpcSignatureReference::GetId (msopc.h)
description: Gets the identifier for the reference.
helpviewer_keywords: ["GetId","GetId method [Open Packaging Conventions]","GetId method [Open Packaging Conventions]","IOpcSignatureReference interface","IOpcSignatureReference interface [Open Packaging Conventions]","GetId method","IOpcSignatureReference.GetId","IOpcSignatureReference::GetId","msopc/IOpcSignatureReference::GetId","opc.iopcsignaturereference_getid"]
old-location: opc\iopcsignaturereference_getid.htm
tech.root: OPC
ms.assetid: 741fd38e-910a-42c7-8bd2-006cf29843d9
ms.date: 12/05/2018
ms.keywords: GetId, GetId method [Open Packaging Conventions], GetId method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetId method, IOpcSignatureReference.GetId, IOpcSignatureReference::GetId, msopc/IOpcSignatureReference::GetId, opc.iopcsignaturereference_getid
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
 - IOpcSignatureReference::GetId
 - msopc/IOpcSignatureReference::GetId
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
 - IOpcSignatureReference.GetId
---

# IOpcSignatureReference::GetId


## -description

Gets the identifier for the reference.

## -parameters

### -param referenceId [out, retval]

An identifier for the reference.

If the identifier is not set, <i>referenceId</i> will be the empty string, "".

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
The <i>referenceId</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>referenceId</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

Providing an identifier for a reference is optional. If used, the identifier is serialized as the optional <b>Id</b> attribute  of a <b>Reference</b> element in the signature markup.


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