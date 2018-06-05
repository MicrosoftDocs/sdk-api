---
UID: NF:msopc.IOpcDigitalSignatureManager.Validate
title: IOpcDigitalSignatureManager::Validate
author: windows-sdk-content
description: Validates a specified package signature using a specified certificate.
old-location: opc\iopcdigitalsignaturemanager_validate.htm
old-project: OPC
ms.assetid: 76a37ad6-caa0-4fa3-abc1-2eae63e3134b
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],Validate method, IOpcDigitalSignatureManager.Validate, IOpcDigitalSignatureManager::Validate, Validate, Validate method [Open Packaging Conventions], Validate method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::Validate, opc.iopcdigitalsignaturemanager_validate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcDigitalSignatureManager.Validate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcDigitalSignatureManager::Validate


## -description


Validates a specified package signature using a specified certificate.


## -parameters




### -param signature [in]

An <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointer that represents  the signature to be validated.


### -param certificate [in]

A pointer to a <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure that contains a certificate that is used to validate the signature.


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

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/e523b335-0156-4f47-b55c-b80495587c4f">Digital Certificates</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

