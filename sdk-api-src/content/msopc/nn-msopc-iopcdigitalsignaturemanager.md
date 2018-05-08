---
UID: NN:msopc.IOpcDigitalSignatureManager
title: IOpcDigitalSignatureManager
author: windows-driver-content
description: Provides access to Packaging Digital Signature Interfaces for a package that is represented by Packaging API objects.
old-location: opc\iopcdigitalsignaturemanager.htm
old-project: OPC
ms.assetid: 13e8a7b9-1d25-421b-bc81-adc495e6d9c7
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcDigitalSignatureManager, IOpcDigitalSignatureManager interface [Open Packaging Conventions], IOpcDigitalSignatureManager interface [Open Packaging Conventions],described, msopc/IOpcDigitalSignatureManager, opc.iopcdigitalsignaturemanager
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcDigitalSignatureManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcDigitalSignatureManager interface


## -description


Provides access to <a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a> for a package that is represented by Packaging API objects. These interface methods are called to generate  a signature, or to access and validate existing signatures in the package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcDigitalSignatureManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcDigitalSignatureManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcDigitalSignatureManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c58f9730-b2c2-40cd-8aae-03fbd09f8c76">CreateSigningOptions</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44906f03-806f-400c-a7f3-0da5c330e1ff">GetSignatureEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a> interface pointers, which represent package signatures.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/958cf2e7-0956-489a-904f-01ec00af48d1">GetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">

              Gets an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer that represents the part name of the Digital Signature Origin part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc022b81-f61d-4efa-9c68-f798b2d929c2">RemoveSignature</a>
</td>
<td align="left" width="63%">

              Removes from the package a specified signature part  that stores signature markup.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cacd0ccf-0cb9-41dc-a944-74db8254fd95">ReplaceSignatureXml</a>
</td>
<td align="left" width="63%">

              Replaces the existing signature markup that is stored in a specified signature part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edf1590c-14a2-4887-a2df-20b5b4cb89a6">SetSignatureOriginPartName</a>
</td>
<td align="left" width="63%">

              Sets the part name of the Digital Signature Origin part to the name represented by a specified <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">Sign</a>
</td>
<td align="left" width="63%">

              Signs the package by generating a signature by using the specified certificate and <a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a> interface pointer.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76a37ad6-caa0-4fa3-abc1-2eae63e3134b">Validate</a>
</td>
<td align="left" width="63%">

              Validates a specified package signature using a specified certificate.
            

</td>
</tr>
</table> 


## -remarks



 Before the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">Sign</a> method is called to generate a signature, the <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">IOpcSigningOptions::SetDefaultDigestMethod</a> and <a href="https://msdn.microsoft.com/b567b09a-e688-4c02-8c01-983a307fd0e2">IOpcSigningOptions::SetSignatureMethod</a> methods must be called.

To create an   <b>IOpcDigitalSignatureManager</b> interface pointer, call the <a href="https://msdn.microsoft.com/ec0fe8b6-e968-4bcb-b468-bbf72ffce675">IOpcFactory::CreateDigitalSignatureManager</a> method.

<div class="alert"><b>Important</b>  If the package is modified while the <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">Sign</a> method is being executed, the method may fail or generate an inconsistent signature. To avoid corruption of the package, use the APIs to save the package prior to calling <b>Sign</b>. For information about how to save a package, see  <a href="https://msdn.microsoft.com/120436c8-7a12-4d48-be84-a02bbb672c7f">Saving a Package</a>.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/76a37ad6-caa0-4fa3-abc1-2eae63e3134b">Validate</a> method checks that the specified signature (signed entities and the signature markup) has not been altered since the signature was generated, but does not validate the identity of the signer. <div class="alert"><b>Important</b>  The caller must validate the identity of the signer.</div>
<div> </div>



#### Thread Safety

Packaging objects are not thread-safe.

IOpcSigningOptions
For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/73fd0e47-7503-470d-b649-e4b2ba492bf1">IOpcDigitalSignatureEnumerator</a>



<a href="https://msdn.microsoft.com/0a265a0a-c109-4afc-a0ad-d3ee31757aa1">IOpcFactory</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

