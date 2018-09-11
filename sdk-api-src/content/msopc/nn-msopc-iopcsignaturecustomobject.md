---
UID: NN:msopc.IOpcSignatureCustomObject
title: IOpcSignatureCustomObject
author: windows-sdk-content
description: Represents an application-specific Object element that has been or will be signed.
old-location: opc\iopcsignaturecustomobject.htm
tech.root: OPC
ms.assetid: 4ebb4fbe-66cc-46d9-b548-31177d9f6da9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcSignatureCustomObject, IOpcSignatureCustomObject interface [Open Packaging Conventions], IOpcSignatureCustomObject interface [Open Packaging Conventions],described, msopc/IOpcSignatureCustomObject, opc.iopcsignaturecustomobject
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
 - IOpcSignatureCustomObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureCustomObject interface


## -description


Represents an application-specific <b>Object</b> element that has been or will be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureCustomObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureCustomObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureCustomObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fedb6f47-59b9-4959-91ef-db1fb398aca9">GetXml</a>
</td>
<td align="left" width="63%">
Gets the XML markup of an application-specific <b>Object</b> element.

</td>
</tr>
</table> 


## -remarks



An <b>IOpcSignatureCustomObject</b> interface pointer provides access to the XML markup of the <b>Object</b> element it represents. To access the XML markup of the  <b>Object</b> element, call the <a href="https://msdn.microsoft.com/fedb6f47-59b9-4959-91ef-db1fb398aca9">IOpcSignatureCustomObject::GetXml</a> method.

Serialized application-specific <b>Object</b> elements in signature markup can be added, removed, or modified by replacing the signature markup.

To replace signature markup, call the <a href="https://msdn.microsoft.com/cacd0ccf-0cb9-41dc-a944-74db8254fd95">IOpcDigitalSignatureManager::ReplaceSignatureXml</a> method. The caller must ensure that addition, deletion, or modification of application-specific <b>Object</b> elements does not break the signature.

To sign an application-specific  <b>Object</b> element or a child of the element, create a reference to the element to be signed. Create the reference by calling the <a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">IOpcSignatureReferenceSet::Create</a> method with the <i>referenceUri</i> parameter value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application",  set <i>referenceUri</i> to "#Application".

To create an <b>IOpcSignatureCustomObject</b> interface pointer, call the <a href="https://msdn.microsoft.com/93bf4509-900c-42bc-9834-c8a33cfe7e65">IOpcSignatureCustomObjectSet::Create</a> method.

To access  an <b>IOpcSignatureCustomObject</b> interface pointer, call the <a href="https://msdn.microsoft.com/a0197da5-e613-4aba-8098-901e192051ff">IOpcSignatureCustomObjectEnumerator::GetCurrent</a> method.

When a signature is generated, the markup of application-specific <b>Object</b> element is included in the signature markup.

Application-specific <b>Object</b> elements are not required for package signatures.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/e82caa1e-4cf8-457f-86d9-24f707544199">IOpcSignatureCustomObjectEnumerator</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

