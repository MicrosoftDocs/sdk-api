---
UID: NF:msopc.IOpcDigitalSignatureManager.Validate
title: IOpcDigitalSignatureManager::Validate (msopc.h)
description: Validates a specified package signature using a specified certificate.
helpviewer_keywords: ["IOpcDigitalSignatureManager interface [Open Packaging Conventions]","Validate method","IOpcDigitalSignatureManager.Validate","IOpcDigitalSignatureManager::Validate","Validate","Validate method [Open Packaging Conventions]","Validate method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","msopc/IOpcDigitalSignatureManager::Validate","opc.iopcdigitalsignaturemanager_validate"]
old-location: opc\iopcdigitalsignaturemanager_validate.htm
tech.root: OPC
ms.assetid: 76a37ad6-caa0-4fa3-abc1-2eae63e3134b
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],Validate method, IOpcDigitalSignatureManager.Validate, IOpcDigitalSignatureManager::Validate, Validate, Validate method [Open Packaging Conventions], Validate method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::Validate, opc.iopcdigitalsignaturemanager_validate
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
 - IOpcDigitalSignatureManager::Validate
 - msopc/IOpcDigitalSignatureManager::Validate
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
 - IOpcDigitalSignatureManager.Validate
---

# IOpcDigitalSignatureManager::Validate


## -description

Validates a specified package signature using a specified certificate.

## -parameters

### -param signature [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointer that represents  the signature to be validated.

### -param certificate [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains a certificate that is used to validate the signature.

### -param validationResult [out, retval]

A value that describes the result of the validation check.

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
 At least one of the <i>signature</i>, <i>certificate</i>, and <i>validationResult</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method does not perform security checks on an X.509 Public Key Infrastructure Certificate; the caller must perform the checks for revocation, expiration, certificate chain, and all other necessary checks.

This method checks that the specified signature (signed entities and the signature markup) has not been altered since the signature was generated, but does not validate the identity of the signer. 

<div class="alert"><b>Important</b>  The caller must validate the identity of the signer.</div>
<div> </div>
If there are errors in a package signature, some of these errors may not be exposed until this method is called.


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