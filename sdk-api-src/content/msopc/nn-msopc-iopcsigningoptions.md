---
UID: NN:msopc.IOpcSigningOptions
title: IOpcSigningOptions (msopc.h)
author: windows-sdk-content
description: Provides methods to set and access information required to generate a signature.
old-location: opc\iopcsigningoptions.htm
tech.root: OPC
ms.assetid: 5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions, IOpcSigningOptions interface [Open Packaging Conventions], IOpcSigningOptions interface [Open Packaging Conventions],described, msopc/IOpcSigningOptions, opc.iopcsigningoptions
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcSigningOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSigningOptions interface


## -description


Provides methods to set and access information required to generate a signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSigningOptions</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSigningOptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSigningOptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86f83829-0507-4918-ae7f-71738f985068">GetCertificateEmbeddingOption</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the storage location in the package of the certificate to be used for the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df212397-7ec9-4a42-bebb-61799b7ca78e">GetCertificateSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b4d31cb-f12a-4b51-8b28-470e065e1661">GetCustomObjectSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2222772a-e396-4d78-a7e4-a12f19ec689b">GetCustomReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8ec81e6-7807-4a1e-9e0c-f5512bd605fa">GetDefaultDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the default digest method that will be used to compute digest values for objects to be signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b81b49de-aaee-4224-9f5c-554b51f10cfa">GetSignatureId</a>
</td>
<td align="left" width="63%">
Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d325ed58-9acd-4ebd-9acc-28f8602a53eb">GetSignatureMethod</a>
</td>
<td align="left" width="63%">
Gets the signature method to use to calculate and encrypt the hash value of the <b>SignedInfo</b> element, which will be serialized as the <b>SignatureValue</b> element of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09481639-eea1-4203-932f-e97558408b42">GetSignaturePartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the signature part where the signature markup will be stored.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60e657c3-41a3-4a05-a084-111429b1add9">GetSignaturePartReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/c6f453e4-e0f5-4ecc-b622-6b30778ff719">IOpcSignaturePartReferenceSet</a> interface.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f89327d2-63ff-4b14-bde0-8fdf65f73e37">GetSignatureRelationshipReferenceSet</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69394df9-5382-49eb-9aa2-0785dee10ac4">GetTimeFormat</a>
</td>
<td align="left" width="63%">
Gets the format of the string retrieved by the <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">IOpcDigitalSignature::GetSigningTime</a> method.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afae4b98-c05f-4fa3-bb1e-f9f43ee86e64">SetCertificateEmbeddingOption</a>
</td>
<td align="left" width="63%">
Set the storage location of the certificate to be used for the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">SetDefaultDigestMethod</a>
</td>
<td align="left" width="63%">
Sets the default digest method that will be used to compute digest values for objects to be signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c723d6e8-6af3-41a2-b6dd-d26897495965">SetSignatureId</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">SetSignatureMethod</a>
</td>
<td align="left" width="63%">
Sets the signature method to use to calculate and encrypt the hash value of the <b>SignedInfo</b> element, which will be contained in the <b>SignatureValue</b> element of the signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36d69a11-bfc3-4f0a-a681-4e138751990d">SetSignaturePartName</a>
</td>
<td align="left" width="63%">
Sets the part name of the signature part where the signature markup will be stored.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f8c1dbe-6347-4013-bda6-5e08c9d6921d">SetTimeFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the string retrieved by the <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">IOpcDigitalSignature::GetSigningTime</a> method.
            

</td>
</tr>
</table> 


## -remarks



To generate a signature, call the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignatureManager::Sign</a> method with the <i>signingOptions</i> parameter value set to an <b>IOpcSigningOptions</b> interface pointer.

To create an <b>IOpcSigningOptions</b> interface pointer, call the <a href="https://msdn.microsoft.com/c58f9730-b2c2-40cd-8aae-03fbd09f8c76">IOpcDigitalSignatureManager::CreateSigningOptions</a> method.

The caller must set a default for the digest method and signature method before generating a signature. To set a default digest method, call the <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">SetDefaultDigestMethod</a> method. To set a signature method, call the <a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">SetSignatureMethod</a> method.

To get an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface pointer, call the <a href="https://msdn.microsoft.com/1b4d31cb-f12a-4b51-8b28-470e065e1661">GetCustomObjectSet</a> method. The interface pointers in the set represent application-specific <b>Object</b> elements.

 To get an <a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a> interface pointer, call the <a href="https://msdn.microsoft.com/2222772a-e396-4d78-a7e4-a12f19ec689b">GetCustomReferenceSet</a> method. The interface pointers in the set represent references to application-specific <b>Object</b> elements or their children that will be signed when the signature is generated.

The default location of the certificate is <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>. To change this value, call the <a href="https://msdn.microsoft.com/afae4b98-c05f-4fa3-bb1e-f9f43ee86e64">SetCertificateEmbeddingOption</a> method.

The default format of the signing time string is <b>OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS</b>. To change the format of the signing time string, call the <a href="https://msdn.microsoft.com/3f8c1dbe-6347-4013-bda6-5e08c9d6921d">SetTimeFormat</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

