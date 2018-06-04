---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOpcDigitalSignature::GetPackageObjectReference


## -description


Gets an  <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.


## -parameters




### -param packageObjectReference [out, retval]

An <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a> interface pointer that represents the reference to the package-specific <b>Object</b> element that has been signed.


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
The <i>packageObjectReference</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The   <a href="https://msdn.microsoft.com/2ce40bc7-754a-4f69-9348-75603e2257a4">IOpcSignatureReference</a>   interface pointer received in the <i>packageObjectReference</i> parameter represents the <b>Reference</b> element that has the  <b>URI</b> attribute value set to "#idPackageObject". The <b>URI</b> attribute value of this element is the <b>Id</b> attribute value of the package-specific <b>Object</b> element, prefixed with a pound sign ("#").

When the signature is generated and serialized as signature markup, the reference and the referenced  package-specific <b>Object</b> element are signed. The following markup shows the package-specific <b>Reference</b> element and the package-specific <b>Object</b> element in the resultant signature markup.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;!-- Signature markup. --&gt;
&lt;Signature&gt;
    &lt;SignedInfo&gt;
        [...]
        &lt;!-- A reference to the package-specific &lt;Object&gt; that
        is, or will be, signed. --&gt;
        &lt;Reference URI="#idPackageObject"&gt;
             [...]
        &lt;/Reference&gt;
    &lt;/SignedInfo&gt;
    [...]
    &lt;!-- The package-specific &lt;Object&gt; element. --&gt;
    &lt;Object Id="idPackageObject"&gt;
        &lt;!-- This element contains the &lt;Reference&gt; elements that
        refer to parts and relationships in the package that are
        or will be signed. --&gt;
        &lt;Manifest&gt;
            [...] 
        &lt;/Manifest&gt;
    &lt;/Object&gt;
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



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

