---
UID: NN:msopc.IOpcDigitalSignature
title: IOpcDigitalSignature
author: windows-sdk-content
description: Represents a package digital signature.
old-location: opc\iopcdigitalsignature.htm
old-project: OPC
ms.assetid: cfa38ef6-9d96-4577-a3bf-518784d19ad8
ms.author: windowssdkdev
ms.date: 03/15/2018
ms.keywords: IOpcDigitalSignature, IOpcDigitalSignature interface [Open Packaging Conventions], IOpcDigitalSignature interface [Open Packaging Conventions],described, msopc/IOpcDigitalSignature, opc.iopcdigitalsignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcDigitalSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcDigitalSignature interface


## -description


Represents a  package digital signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcDigitalSignature</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcDigitalSignature</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcDigitalSignature</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59c89909-6e35-4210-b76c-c820a9bb0d8e">GetCanonicalizationMethod</a>
</td>
<td align="left" width="63%">

              Gets the canonicalization method  that was applied to the <b>SignedInfo</b> element of the serialized signature.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b5b803f-fc61-41fa-aa73-eefb1c1d2f00">GetCertificateEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of certificates that are used in the signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1263ca86-8b4f-4be9-a88a-f11e76178d0d">GetCustomObjectEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointers that represent application-specific <b>Object</b> elements in the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cc5ae5d-faef-451d-8ad8-db4b8b5c0e22">GetCustomReferenceEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of the <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers that represent references to application-specific XML elements that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9360d23-1eac-4bb1-ae40-c157f1a79621">GetNamespaces</a>
</td>
<td align="left" width="63%">

              Gets the prefix and namespace mapping of the <b>Signature</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67f4404f-518c-4a47-8c8e-b5b8d13e18cb">GetPackageObjectReference</a>
</td>
<td align="left" width="63%">

              Gets an  <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20eea0ff-dff1-4f95-aaf7-00e5a36503f1">GetSignatureId</a>
</td>
<td align="left" width="63%">

              Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4dfd99f-16d7-4bf1-9852-d6d1fd4a3f06">GetSignatureMethod</a>
</td>
<td align="left" width="63%">

              Gets the signature method used to calculate the value in the <b>SignatureValue</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a7f9413-d44d-4d3d-bb4e-01ef14ee7a1c">GetSignaturePartName</a>
</td>
<td align="left" width="63%">

              Gets the part name of the part that contains the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8d1507e-b72f-4eb7-bd3d-4f4a26516c18">GetSignaturePartReferenceEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers, which represent references to parts that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffb74828-1177-4c3d-8a8c-e40bb0c4cbf0">GetSignatureRelationshipReferenceEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c918d156-ad32-4a0c-83cc-dd37fe884744">GetSignatureValue</a>
</td>
<td align="left" width="63%">

              Gets the decoded value in the <b>SignatureValue</b> element of the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b495661-32ed-4010-a945-7e638f30f4f2">GetSignatureXml</a>
</td>
<td align="left" width="63%">

              Gets the signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">GetSigningTime</a>
</td>
<td align="left" width="63%">
Gets a string that indicates the time at which the signature was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df142c4d-27dc-4db3-9a37-78c5703c8119">GetTimeFormat</a>
</td>
<td align="left" width="63%">

              Gets the format of the string returned by the <a href="https://msdn.microsoft.com/8054eba8-ca53-42e4-9105-ef7cf20637c1">GetSigningTime</a> method.
            

</td>
</tr>
</table> 


## -remarks



To generate a signature and create an   <b>IOpcDigitalSignature</b> interface pointer, call the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignatureManager::Sign</a> method.

To access generated signature by using an   <b>IOpcDigitalSignature</b> interface pointer, call the <a href="https://msdn.microsoft.com/2e211822-9fd8-424c-bd0c-c5c81f9abc0b">IOpcDigitalSignatureEnumerator::GetCurrent</a> method.

When a signature is generated, this information is serialized in the XML markup of the signature (signature markup).  The signature markup that results is stored in a signature part.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/73fd0e47-7503-470d-b649-e4b2ba492bf1">IOpcDigitalSignatureEnumerator</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<a href="https://msdn.microsoft.com/9b8ff585-5795-48ce-b2fd-a49e3d34ccb9">OPC_SIGNATURE_TIME_FORMAT</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

