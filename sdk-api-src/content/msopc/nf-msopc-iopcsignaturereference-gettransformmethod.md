---
UID: NF:msopc.IOpcSignatureReference.GetTransformMethod
title: IOpcSignatureReference::GetTransformMethod (msopc.h)
description: Gets the canonicalization method to use on the referenced XML element, when the element is signed.
helpviewer_keywords: ["GetTransformMethod","GetTransformMethod method [Open Packaging Conventions]","GetTransformMethod method [Open Packaging Conventions]","IOpcSignatureReference interface","IOpcSignatureReference interface [Open Packaging Conventions]","GetTransformMethod method","IOpcSignatureReference.GetTransformMethod","IOpcSignatureReference::GetTransformMethod","msopc/IOpcSignatureReference::GetTransformMethod","opc.iopcsignaturereference_gettransformmethod"]
old-location: opc\iopcsignaturereference_gettransformmethod.htm
tech.root: OPC
ms.assetid: f3f3f6a8-c15e-420a-b56d-5dac0a054fac
ms.date: 12/05/2018
ms.keywords: GetTransformMethod, GetTransformMethod method [Open Packaging Conventions], GetTransformMethod method [Open Packaging Conventions],IOpcSignatureReference interface, IOpcSignatureReference interface [Open Packaging Conventions],GetTransformMethod method, IOpcSignatureReference.GetTransformMethod, IOpcSignatureReference::GetTransformMethod, msopc/IOpcSignatureReference::GetTransformMethod, opc.iopcsignaturereference_gettransformmethod
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
 - IOpcSignatureReference::GetTransformMethod
 - msopc/IOpcSignatureReference::GetTransformMethod
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
 - IOpcSignatureReference.GetTransformMethod
---

# IOpcSignatureReference::GetTransformMethod


## -description

Gets the canonicalization method to use on the referenced XML element, when the element is signed.

## -parameters

### -param transformMethod [out, retval]

 The canonicalization method to use on the referenced XML element, when the element is signed.

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
The <i>transformMethod</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>