---
UID: NF:msopc.IOpcDigitalSignatureManager.Sign
title: IOpcDigitalSignatureManager::Sign
author: windows-sdk-content
description: Signs the package by generating a signature by using the specified certificate and IOpcSigningOptions interface pointer.
old-location: opc\iopcdigitalsignaturemanager_sign.htm
tech.root: OPC
ms.assetid: 5d40cae4-67d5-40a6-bd63-cf6243a703eb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],Sign method, IOpcDigitalSignatureManager.Sign, IOpcDigitalSignatureManager::Sign, Sign, Sign method [Open Packaging Conventions], Sign method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::Sign, opc.iopcdigitalsignaturemanager_sign
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcDigitalSignatureManager.Sign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignatureManager::Sign


## -description


    Signs the package by generating a signature by using the specified certificate and <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer. The resultant signature is represented by an <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointer.


## -parameters




### -param certificate [in]

A pointer to a <a href="http://msdn.microsoft.com/en-us/library/aa377189(vs.85).aspx">CERT_CONTEXT</a> structure that contains the certificate.


### -param signingOptions [in]

An <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer that is used to generate the signature.


### -param digitalSignature [out, retval]

A new <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointer that represents the signature.


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
The default digest method has not been set; to set it, call <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">IOpcSigningOptions::SetDefaultDigestMethod</a>.

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
The signature's time format is not a valid <a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a> enumeration value.

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
An indicated  relationship signing option is not a valid <a href="https://msdn.microsoft.com/b6a83730-459a-4119-a013-7d670e659c32">OPC_RELATIONSHIPS_SIGNING_OPTION</a> enumeration value.

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
The signature method has not been set.  Call <a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">IOpcSigningOptions::SetSignatureMethod</a> to set the signature method.

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
An <b>HRESULT</b> error code from a <a href="https://msdn.microsoft.com/0468cece-6449-4772-82c9-e3f410c34e46">Cryptography</a> API.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Windows Web Services error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from a <a href="wsw.web_services_for_windows_error_codes">Windows Web Services</a> API.

</td>
</tr>
</table>
 




## -remarks



This method uses Packaging objects to make changes to a package. The resultant changes are not saved until the package itself is  saved.

 Before this  method is called to generate a signature, call the <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">IOpcSigningOptions::SetDefaultDigestMethod</a> and <a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">IOpcSigningOptions::SetSignatureMethod</a> methods.

To create an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer, which is required by this method, call the <a href="https://msdn.microsoft.com/c58f9730-b2c2-40cd-8aae-03fbd09f8c76">CreateSigningOptions</a> method. 

<div class="alert"><b>Important</b>  If the package is modified while this method is being executed, <b>Sign</b> may fail or generate an inconsistent signature. To avoid corruption of the package, use the APIs to save the package prior to calling <b>Sign</b>. For information about how to save a package, see  <a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a>.</div>
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

If <b>Sign</b> is successful, digest values are calculated for signed enitities, and the generated signature is serialized as signature markup. Possible signed entities include the <b>Signature</b> element, references, parts, relationships,  and package-specific and application-specific <b>Object</b> elements.

Errors that are introduced into a package signature when the caller is using the <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface to set signature information may not be exposed until <b>Sign</b> is called.


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



<a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a>
 

 

