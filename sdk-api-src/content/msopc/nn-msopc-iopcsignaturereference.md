---
UID: NN:msopc.IOpcSignatureReference
title: IOpcSignatureReference
author: windows-sdk-content
description: Represents a reference to XML markup that has been or will be signed.
old-location: opc\iopcsignaturereference.htm
tech.root: OPC
ms.assetid: 2ce40bc7-754a-4f69-9348-75603e2257a4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOpcSignatureReference, IOpcSignatureReference interface [Open Packaging Conventions], IOpcSignatureReference interface [Open Packaging Conventions],described, msopc/IOpcSignatureReference, opc.iopcsignaturereference
ms.prod: windows
ms.technology: windows-sdk
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
 - IOpcSignatureReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureReference interface


## -description


Represents a reference to XML markup that has been or will be signed. This referenced XML markup is serialized in the signature markup when a signature is generated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/438adeba-bf5f-4f87-ab4c-c370e58565ce">GetDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the digest method to use on the referenced XML element, when the element is signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bb46de1-63af-4ac1-b37b-42a2b174b590">GetDigestValue</a>
</td>
<td align="left" width="63%">
Gets the digest value that is calculated for the referenced XML element when the element is signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/741fd38e-910a-42c7-8bd2-006cf29843d9">GetId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the reference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3f3f6a8-c15e-420a-b56d-5dac0a054fac">GetTransformMethod</a>
</td>
<td align="left" width="63%">
Gets the canonicalization method to use on the referenced XML element, when the element is signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7402f031-b06c-4fc6-bb54-ad9fc28600b3">GetType</a>
</td>
<td align="left" width="63%">
Gets a string that indicates the type of the referenced XML  element.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dd02f48-9b49-4e74-b0cf-c51c0a594437">GetUri</a>
</td>
<td align="left" width="63%">
Gets the URI of the referenced XML element.
            

</td>
</tr>
</table> 


## -remarks



To create 
				an <b>IOpcSignatureReference</b> interface pointer, call the <a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">IOpcSignatureReferenceSet::Create</a> method. <b>IOpcSignatureReferenceSet::Create</b> does not create the reference to the package-specific <b>Object</b> element; that reference is created automatically when the signature is generated.

To access an <b>IOpcSignatureReference</b> interface pointer, call the <a href="https://msdn.microsoft.com/3bbf1a09-4d59-466f-ac48-2e4e67232ed4">IOpcSignatureReferenceEnumerator::GetCurrent</a> method. <b>IOpcSignatureReferenceEnumerator::GetCurrent</b> does not access the reference to the package-specific <b>Object</b> element; call the <a href="https://msdn.microsoft.com/67f4404f-518c-4a47-8c8e-b5b8d13e18cb">IOpcDigitalSignature::GetPackageObjectReference</a> method to access that  reference.

The interface provides methods to access information about the reference itself, and referenced XML element. The referenced element can be the package-specific <b>Object</b> element, an application-specific  <b>Object</b> element, or a child element of an application-specific  <b>Object</b>. 

 When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has its <b>URI</b> attribute value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application" the <b>URI</b> attribute of the <b>Reference</b> element is set to "#Application" as shown in the following markup.

The following signature markup shows a serialized reference to a signed, application-specific <b>Object</b> element.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Signature Id="SignatureId" xmlns="http://www.w3.org/2000/09/xmldsig#"&gt;
    &lt;SignedInfo&gt;
        [...]
        &lt;Reference URI="#idPackageObject" ...&gt;
            [...]
        &lt;/Reference&gt;
        &lt;!-- This reference indicates that the application-specific
        Object element was signed when the signature was generated.--&gt;
        &lt;Reference URI="#Application" ...&gt;
            [...]
        &lt;/Reference&gt;
    &lt;/SignedInfo&gt;
    [...]
    &lt;Object Id="idPackageObject" ...&gt;
        [...]
    &lt;/Object&gt;
    &lt;!-- This application-specific &lt;Object&gt; element was signed when the
    signature was generated. --&gt;
    &lt;Object Id="Application"&gt;
        [...]
    &lt;/Object&gt;
&lt;/Signature&gt;</pre>
</td>
</tr>
</table></span></div>
The following signature markup shows a serialized reference to a signed, child element of an application-specific <b>Object</b> element.<div class="alert"><b>Note</b>  More than one child element of an application-specific <b>Object</b> can be referenced for signing.</div>
<div> </div>


<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;Signature Id="SignatureId" xmlns="http://www.w3.org/2000/09/xmldsig#"&gt;
    &lt;SignedInfo&gt;
        [...]
        &lt;Reference URI="#idPackageObject" ...&gt;
            [...]
        &lt;/Reference&gt;
        &lt;!-- This reference indicates that MyElement in the application
        -specific Object element was signed when the signature was
        generated. --&gt;
        &lt;Reference URI="#MyElementId" ...&gt;
            [...]
        &lt;/Reference&gt;
    &lt;/SignedInfo&gt;
    [...]
    &lt;Object Id="idPackageObject" ...&gt;
        [...]
    &lt;/Object&gt;
    &lt;Object Id="Application"&gt;
        [...]
            &lt;!-- This element is signed. --&gt;
            &lt;MyElement Id="MyElementId"&gt;
                [...]
            &lt;/MyElement&gt;
        [...]
    &lt;/Object&gt;
&lt;/Signature&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

