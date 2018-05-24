---
UID: NF:msopc.IOpcSignatureReferenceSet.Create
title: IOpcSignatureReferenceSet::Create
author: windows-driver-content
description: Creates an IOpcSignatureReference interface pointer that represents a reference to an XML element to be signed.
old-location: opc\iopcsignaturereferenceset_create.htm
old-project: OPC
ms.assetid: 5e943769-a043-4354-80e7-d471a1dbde7a
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignatureReferenceSet interface, IOpcSignatureReferenceSet interface [Open Packaging Conventions],Create method, IOpcSignatureReferenceSet.Create, IOpcSignatureReferenceSet::Create, msopc/IOpcSignatureReferenceSet::Create, opc.iopcsignaturereferenceset_create
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcSignatureReferenceSet.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureReferenceSet::Create


## -description


Creates an <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents a reference to an XML element to be signed.


## -parameters




### -param referenceUri [in]

The URI of  the referenced XML element.

Set the value of this parameter to a URI that represents "#" followed by  the <b>Id</b> attribute value of the referenced element: "#<i>&lt;elementIdValue&gt;</i>".

For examples, see the Remarks section.


### -param referenceId [in]

The <b>Id</b> attribute of the <b>Reference</b> element that represents the reference in signature  markup. To omit the  <b>Id</b> attribute, set this parameter value to  <b>NULL</b>.


### -param type [in]

The <b>Type</b> attribute of the <b>Reference</b> element that represents the reference in signature markup. To omit the <b>Type</b> attribute, set this parameter value to  <b>NULL</b>.


### -param digestMethod [in]

The digest method to be used for the XML markup to be referenced. To use the default digest method,  set this parameter value to  <b>NULL</b>.

<div class="alert"><b>Important</b>  The default digest method must be set by calling the <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">IOpcSigningOptions::SetDefaultDigestMethod</a> method before <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignatureManager::Sign</a> is called.</div>
<div> </div>

### -param transformMethod [in]

The canonicalization method to be used for the XML markup to be referenced.


### -param reference [out, retval]

A new <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents the reference to  the XML element to be signed.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>transformMethod</i> parameter is not a valid <a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>referenceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_PACKAGE_REFERENCE_URI_RESERVED</b></dt>
<dt>0x80510025</dt>
</dl>
</td>
<td width="60%">
The reserved <b>URI</b> attribute value of the signature's <b>Reference</b> element to the package <b>Object</b> is being used as the <b>URI</b> attribute value of a <b>Reference</b> to a custom <b>Object</b> element.

</td>
</tr>
</table>
 




## -remarks



This method creates a reference to an XML element that is signed when the signature is generated. The referenced element can be either an application-specific <b>Object</b> element or a child of an application-specific <b>Object</b>.

To reference an XML element for signing, set the <i>referenceUri</i> parameter value to a URI that represents "#" followed by  the <b>Id</b> attribute value of the referenced element, as shown in the following table.<table>
<tr>
<th><i>referenceUri</i> Value as String</th>
<th>Referenced Element</th>
<th>Element Description</th>
</tr>
<tr>
<td>"#<i>idMyCustomObject</i>"</td>
<td>"&lt;Object Id="<i>idMyCustomObject</i>"&gt;<i>...</i>&lt;/Object&gt;"</td>
<td>
An application-specific <b>Object</b> element.

</td>
</tr>
<tr>
<td>"#<i>idMyElement</i>"</td>
<td>"&lt;Object&gt;&lt;<i>MyElement</i> Id="<i>idMyElement</i>"&gt;<i>...</i>&lt;/<i>MyElement</i>&gt;...&lt;/Object&gt;"</td>
<td>
A child element of an application-specific <b>Object</b>.

</td>
</tr>
</table>
 



This method does not create the reference to the package-specific <b>Object</b> element to be signed; that reference is created automatically when the signature is generated.

When an <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

