---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureXml
title: IOpcDigitalSignature::GetSignatureXml (msopc.h)
description: Gets the signature markup.
helpviewer_keywords: ["GetSignatureXml","GetSignatureXml method [Open Packaging Conventions]","GetSignatureXml method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignatureXml method","IOpcDigitalSignature.GetSignatureXml","IOpcDigitalSignature::GetSignatureXml","msopc/IOpcDigitalSignature::GetSignatureXml","opc.iopcdigitalsignature_getsignaturexml"]
old-location: opc\iopcdigitalsignature_getsignaturexml.htm
tech.root: OPC
ms.assetid: 7b495661-32ed-4010-a945-7e638f30f4f2
ms.date: 12/05/2018
ms.keywords: GetSignatureXml, GetSignatureXml method [Open Packaging Conventions], GetSignatureXml method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureXml method, IOpcDigitalSignature.GetSignatureXml, IOpcDigitalSignature::GetSignatureXml, msopc/IOpcDigitalSignature::GetSignatureXml, opc.iopcdigitalsignature_getsignaturexml
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
 - IOpcDigitalSignature::GetSignatureXml
 - msopc/IOpcDigitalSignature::GetSignatureXml
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
 - IOpcDigitalSignature.GetSignatureXml
---

# IOpcDigitalSignature::GetSignatureXml


## -description

Gets the signature markup.

## -parameters

### -param signatureXml [out]

A pointer to a buffer that contains the signature markup.

### -param count [out]

The size of the <i>signatureXml</i> buffer.

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

This method allocates memory used by the buffer returned in <i>signatureXml</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.


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