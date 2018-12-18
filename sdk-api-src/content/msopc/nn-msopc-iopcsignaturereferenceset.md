---
UID: NN:msopc.IOpcSignatureReferenceSet
title: IOpcSignatureReferenceSet
author: windows-sdk-content
description: An unordered set of IOpcSignatureReference interface pointers that represent references to XML elements to be signed.
old-location: opc\iopcsignaturereferenceset.htm
tech.root: OPC
ms.assetid: 7955ac86-de6e-4911-a107-a1617c14e685
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOpcSignatureReferenceSet, IOpcSignatureReferenceSet interface [Open Packaging Conventions], IOpcSignatureReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignatureReferenceSet, opc.iopcsignaturereferenceset
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
 - IOpcSignatureReferenceSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureReferenceSet interface


## -description


An unordered set of <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers that represent references to XML elements  to be signed.  An XML element to be signed can be either an application-specific <b>Object</b> element or a child element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureReferenceSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureReferenceSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureReferenceSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">Create</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents a reference to an XML element to be signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62e47da4-9486-41f4-9e56-23288c0c406b">Delete</a>
</td>
<td align="left" width="63%">
Deletes a specified <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer from the set.
              
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4c39119-7317-408c-9173-efd6d449002e">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointers  in the set.
            

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">Create</a> method creates a reference to an application-specific <b>Object</b> element or a child of an application-specific <b>Object</b> that is signed when the signature is generated. <b>Create</b> does not create the reference to the package-specific <b>Object</b> element to be signed; that reference is created automatically when the signature is generated.

When an <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.

To access an <b>IOpcSignatureReferenceSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/2222772a-e396-4d78-a7e4-a12f19ec689b">IOpcSigningOptions::GetCustomReferenceSet</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

