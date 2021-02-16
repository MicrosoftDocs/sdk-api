---
UID: NF:msopc.IOpcDigitalSignature.GetCanonicalizationMethod
title: IOpcDigitalSignature::GetCanonicalizationMethod (msopc.h)
description: Gets the canonicalization method that was applied to the SignedInfo element of the serialized signature.
helpviewer_keywords: ["GetCanonicalizationMethod","GetCanonicalizationMethod method [Open Packaging Conventions]","GetCanonicalizationMethod method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetCanonicalizationMethod method","IOpcDigitalSignature.GetCanonicalizationMethod","IOpcDigitalSignature::GetCanonicalizationMethod","msopc/IOpcDigitalSignature::GetCanonicalizationMethod","opc.iopcdigitalsignature_getcanonicalizationmethod"]
old-location: opc\iopcdigitalsignature_getcanonicalizationmethod.htm
tech.root: OPC
ms.assetid: 59c89909-6e35-4210-b76c-c820a9bb0d8e
ms.date: 12/05/2018
ms.keywords: GetCanonicalizationMethod, GetCanonicalizationMethod method [Open Packaging Conventions], GetCanonicalizationMethod method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetCanonicalizationMethod method, IOpcDigitalSignature.GetCanonicalizationMethod, IOpcDigitalSignature::GetCanonicalizationMethod, msopc/IOpcDigitalSignature::GetCanonicalizationMethod, opc.iopcdigitalsignature_getcanonicalizationmethod
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
 - IOpcDigitalSignature::GetCanonicalizationMethod
 - msopc/IOpcDigitalSignature::GetCanonicalizationMethod
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
 - IOpcDigitalSignature.GetCanonicalizationMethod
---

# IOpcDigitalSignature::GetCanonicalizationMethod


## -description

Gets the canonicalization method  that was applied to the <b>SignedInfo</b> element of the serialized signature.

## -parameters

### -param canonicalizationMethod [out, retval]

An <a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>  value that specifies the canonicalization method that was applied to the <b>SignedInfo</b> element of the signature markup when the signature was generated.

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
The <i>canonicalizationMethod</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When using the APIs to generate a signature, the C14N canonicalization method that removes comments is applied to the <b>SignedInfo</b> element. This method corresponds to the <b>OPC_CANONICALIZATION_C14N</b> enum value.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>