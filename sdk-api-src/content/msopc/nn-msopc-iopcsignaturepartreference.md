---
UID: NN:msopc.IOpcSignaturePartReference
title: IOpcSignaturePartReference
author: windows-sdk-content
description: Represents a reference to a part that has been or will be signed.
old-location: opc\iopcsignaturepartreference.htm
old-project: OPC
ms.assetid: b4bbf854-96b4-412b-a22d-c810423a3752
ms.author: windowssdkdev
ms.date: 03/15/2018
ms.keywords: IOpcSignaturePartReference, IOpcSignaturePartReference interface [Open Packaging Conventions], IOpcSignaturePartReference interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReference, opc.iopcsignaturepartreference
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
 - IOpcSignaturePartReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignaturePartReference interface


## -description


Represents a reference to a part that has been or will be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignaturePartReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignaturePartReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignaturePartReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1384a0ab-d2dc-49c6-b180-648e256a875d">GetContentType</a>
</td>
<td align="left" width="63%">
Gets the content type of the referenced part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/750aec1a-92b4-4c70-8c17-c15c9536bc41">GetDigestMethod</a>
</td>
<td align="left" width="63%">
              Gets the digest method to use on part content of the referenced part when the part is signed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43ae8891-34fb-46cf-8b61-f7d1bd67a2d2">GetDigestValue</a>
</td>
<td align="left" width="63%">
Gets the digest value that is calculated for part content of the referenced part when  the part is signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf34361f-da74-4785-8e5b-8b9caf809a41">GetPartName</a>
</td>
<td align="left" width="63%">
Gets the part name of the referenced part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74cf5d3b-a350-4574-972d-1907562aece5">GetTransformMethod</a>
</td>
<td align="left" width="63%">
Gets the canonicalization method to use on part content of a referenced part when the part is signed.

</td>
</tr>
</table> 


## -remarks



Only parts that can be represented by the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface can be referenced by an <b>IOpcSignaturePartReference</b> interface pointer. Relationships parts are referenced for signing  by a pointer to the <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface. To create an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">IOpcSignatureRelationshipReferenceSet::Create</a> method.

To create 
				an <b>IOpcSignaturePartReference</b> interface pointer, call the <a href="https://msdn.microsoft.com/63162b37-0262-4d92-a14f-726fe4c87cc1">IOpcSignaturePartReferenceSet::Create</a> method.

To access an <b>IOpcSignaturePartReference</b> interface pointer, call the <a href="https://msdn.microsoft.com/ce5e90dd-9bf3-4632-a957-f468bf91415d">IOpcSignaturePartReferenceEnumerator::GetCurrent</a> method.

The interface provides methods to access information about the referenced part and the reference itself. When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has its <b>URI</b> attribute value set to the part name of the referenced part.

The following markup shows that these <b>Reference</b> elements are children of the <b>Manifest</b> element in signature markup.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>// Signature XML markup
&lt;Signature&gt;
	[...]
	// Package-specific &lt;Object&gt;
	&lt;Object Id="idPackageObject"&gt;
		// This &lt;Manifest&gt; element contains only one signed part. 
		&lt;Manifest&gt;
			// A reference to a signed part.
			&lt;Reference URI="aPartName"&gt;
				[...]
			&lt;/Reference&gt;
		&lt;/Manifest&gt;
		[...]
	&lt;/Object&gt;
	[...]
&lt;/Signature&gt;</pre>
</td>
</tr>
</table></span></div>

#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8a54debe-3ac6-471d-b5a5-c3512da4d079">IOpcSignaturePartReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/c6f453e4-e0f5-4ecc-b622-6b30778ff719">IOpcSignaturePartReferenceSet</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

