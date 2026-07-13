---
UID: NF:msopc.IOpcDigitalSignatureManager.Sign
title: IOpcDigitalSignatureManager::Sign (msopc.h)
description: Signs the package by generating a signature by using the specified certificate and IOpcSigningOptions interface pointer.
helpviewer_keywords: ["IOpcDigitalSignatureManager interface [Open Packaging Conventions]","Sign method","IOpcDigitalSignatureManager.Sign","IOpcDigitalSignatureManager::Sign","Sign","Sign method [Open Packaging Conventions]","Sign method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","msopc/IOpcDigitalSignatureManager::Sign","opc.iopcdigitalsignaturemanager_sign"]
old-location: opc\iopcdigitalsignaturemanager_sign.htm
tech.root: OPC
ms.assetid: 5d40cae4-67d5-40a6-bd63-cf6243a703eb
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],Sign method, IOpcDigitalSignatureManager.Sign, IOpcDigitalSignatureManager::Sign, Sign, Sign method [Open Packaging Conventions], Sign method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::Sign, opc.iopcdigitalsignaturemanager_sign
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
 - IOpcDigitalSignatureManager::Sign
 - msopc/IOpcDigitalSignatureManager::Sign
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
 - IOpcDigitalSignatureManager.Sign
---

# IOpcDigitalSignatureManager::Sign


## -description

    Signs the package by generating a signature by using the specified certificate and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer. The resultant signature is represented by an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointer.

## -parameters

### -param certificate [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate.

### -param signingOptions [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer that is used to generate the signature.

### -param digitalSignature [out, retval]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointer that represents the signature.

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
At least one of the <i>certificate</i>, <i>signingOptions</i>, and <i>digitalSignature</i> parameters is <b>NULL</b>.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_DEFAULT_DIGEST_METHOD_NOT_SET</b></dt>
<dt>0x80510047</dt>
</dl>
</td>
<td width="60%">
The default digest method has not been set; to set it, call <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">IOpcSigningOptions::SetDefaultDigestMethod</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_DIGEST_VALUE_ERROR</b></dt>
<dt>0x8051001A</dt>
</dl>
</td>
<td width="60%">
Cannot get the  digest value of a package component or an element in the signature markup that was referenced for signing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_OPC_SIGNATURE_TIME_FORMAT</b></dt>
<dt>0x80510024</dt>
</dl>
</td>
<td width="60%">
The signature's time format is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_signature_time_format">OPC_SIGNATURE_TIME_FORMAT</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_RELATIONSHIPS_SIGNING_OPTION</b></dt>
<dt>0x80510023</dt>
</dl>
</td>
<td width="60%">
An indicated  relationship signing option is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_relationships_signing_option">OPC_RELATIONSHIPS_SIGNING_OPTION</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_CORRUPT</b></dt>
<dt>0x80510019</dt>
</dl>
</td>
<td width="60%">
A signature in the package is not properly formed. Cannot get the signature value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_METHOD_NOT_SET</b></dt>
<dt>0x80510046</dt>
</dl>
</td>
<td width="60%">
The signature method has not been set.  Call <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">IOpcSigningOptions::SetSignatureMethod</a> to set the signature method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_PART</b></dt>
<dt>0x80510018</dt>
</dl>
</td>
<td width="60%">
The specified part does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Cryptography error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a <a href="/windows/desktop/SecCrypto/cryptography-return-values">Cryptography</a> API.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Windows Web Services error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a <a href="/windows/desktop/wsw/portal">Windows Web Services</a> API.

</td>
</tr>
</table>

## -remarks

This method uses Packaging objects to make changes to a package. The resultant changes are not saved until the package itself is  saved.

 Before this  method is called to generate a signature, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">IOpcSigningOptions::SetDefaultDigestMethod</a> and <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturemethod">IOpcSigningOptions::SetSignatureMethod</a> methods.

To create an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface pointer, which is required by this method, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-createsigningoptions">CreateSigningOptions</a> method. 

<div class="alert"><b>Important</b>  If the package is modified while this method is being executed, <b>Sign</b> may fail or generate an inconsistent signature. To avoid corruption of the package, use the APIs to save the package prior to calling <b>Sign</b>. For information about how to save a package, see  <a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a>.</div>
<div> </div>
This method may create the following parts and relationships:<ul>
<li>The Digital Signature Origin part</li>
<li>The package relationship of the digital signature origin relationship type</li>
<li>One signature part that contains signature markup</li>
<li>One or more part that contains a certificate</li>
<li>One relationship that targets a signature part and that has the Digital Signature Origin part as its source</li>
<li>One or more relationship that targets a signature part that contains a certificate and that has another signature part as its source</li>
</ul>


If <b>Sign</b> fails, any of the above parts and relationships may be represented, in the package, by Packaging objects. If the method returns the <b>OPC_E_DS_SIGNATURE_METHOD_NOT_SET</b> or <b>OPC_E_DS_DEFAULT_DIGEST_METHOD_NOT_SET</b> error code, the package has not been altered.

If <b>Sign</b> is successful, digest values are calculated for signed entities, and the generated signature is serialized as signature markup. Possible signed entities include the <b>Signature</b> element, references, parts, relationships,  and package-specific and application-specific <b>Object</b> elements.

Errors that are introduced into a package signature when the caller is using the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a> interface to set signature information may not be exposed until <b>Sign</b> is called.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/windows/desktop/SecCrypto/digital-certificates">Digital Certificates</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/saving-a-package">Saving a Package</a>