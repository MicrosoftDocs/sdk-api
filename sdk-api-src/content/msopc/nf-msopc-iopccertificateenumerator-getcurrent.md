---
UID: NF:msopc.IOpcCertificateEnumerator.GetCurrent
title: IOpcCertificateEnumerator::GetCurrent (msopc.h)
description: Gets the CERT_CONTEXT structure at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [Open Packaging Conventions]","GetCurrent method [Open Packaging Conventions]","IOpcCertificateEnumerator interface","IOpcCertificateEnumerator interface [Open Packaging Conventions]","GetCurrent method","IOpcCertificateEnumerator.GetCurrent","IOpcCertificateEnumerator::GetCurrent","msopc/IOpcCertificateEnumerator::GetCurrent","opc.iopccertificateenumerator_getcurrent"]
old-location: opc\iopccertificateenumerator_getcurrent.htm
tech.root: OPC
ms.assetid: edd2afc1-cafd-4a52-b2df-1a1fcdf1d6fa
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcCertificateEnumerator interface, IOpcCertificateEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcCertificateEnumerator.GetCurrent, IOpcCertificateEnumerator::GetCurrent, msopc/IOpcCertificateEnumerator::GetCurrent, opc.iopccertificateenumerator_getcurrent
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
 - IOpcCertificateEnumerator::GetCurrent
 - msopc/IOpcCertificateEnumerator::GetCurrent
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
 - IOpcCertificateEnumerator.GetCurrent
---

# IOpcCertificateEnumerator::GetCurrent


## -description

Gets the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure at the current position of the enumerator.

## -parameters

### -param certificate [out, retval]

A  pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.
            If the method succeeds, call the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function to free the memory of the structure.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>Return code/value</th>
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
The <i>partReference</i> parameter is <b>NULL</b>.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_EXTERNAL_SIGNATURE</b></dt>
<dt>0x8051001E</dt>
</dl>
</td>
<td width="60%">
A relationship whose target is a  Signature part has the external target mode; Signature parts must be inside of the package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_CERTIFICATE_RELATIONSHIP</b></dt>
<dt>0x8051001D</dt>
</dl>
</td>
<td width="60%">
A relationship of type  digital signature certificate has the external target mode.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_RELATIONSHIP_TRANSFORM_XML</b></dt>
<dt>0x80510021</dt>
</dl>
</td>
<td width="60%">
A <b>Transform</b> element that indicates the use of the relationships transform and  the selection criteria for the transform does not conform to the schema specified in the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_CERTIFICATE_PART</b></dt>
<dt>0x80510056</dt>
</dl>
</td>
<td width="60%">
The part that contains the certificate and is the target of a relationship of type digital signature certificate does not exist.

For more information about this relationship type, see the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_PROPERTY_MISSING_TARGET</b></dt>
<dt>0x80510045</dt>
</dl>
</td>
<td width="60%">
The <b>SignatureProperty</b> element is missing the required <b>Target</b> attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_UNEXPECTED_CONTENT_TYPE</b></dt>
<dt>0x80510005</dt>
</dl>
</td>
<td width="60%">
Either the content type of a part differed from the expected content type (specified in the OPC, <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 Part 2</a>), or the part content did not match the part's  content type.

</td>
</tr>
</table>

## -remarks

If the certificate represented by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure is corrupted or is not an X.509 certificate, this method will return an error; further,  the signing policy used by the caller dictates whether the signature will still be validated. After this kind of error is returned, calls to the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext">MoveNext</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-moveprevious">MovePrevious</a> method will continue to iterate through the enumerator.

When an enumerator is created, the current position precedes the first pointer of the enumerator. To set the current position to the first pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext">MoveNext</a> method after the enumerator is created.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/certificates">Certificates</a>



<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator">IOpcCertificateEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>