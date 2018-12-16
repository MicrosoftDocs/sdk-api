---
UID: NF:msopc.IOpcSignatureCustomObjectSet.Create
title: IOpcSignatureCustomObjectSet::Create
author: windows-sdk-content
description: Creates an IOpcSignatureCustomObject interface pointer to represent an application-specific Object element in the signature, and adds the new interface to the set.
old-location: opc\iopcsignaturecustomobjectset_create.htm
tech.root: OPC
ms.assetid: 93bf4509-900c-42bc-9834-c8a33cfe7e65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignatureCustomObjectSet interface, IOpcSignatureCustomObjectSet interface [Open Packaging Conventions],Create method, IOpcSignatureCustomObjectSet.Create, IOpcSignatureCustomObjectSet::Create, msopc/IOpcSignatureCustomObjectSet::Create, opc.iopcsignaturecustomobjectset_create
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
 - IOpcSignatureCustomObjectSet.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureCustomObjectSet::Create


## -description


Creates an <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer to represent an application-specific <b>Object</b> element in the signature, and adds the new interface to the set.


## -parameters




### -param xmlMarkup [in]

A buffer that contains the XML markup for the <b>Object</b> element to be represented.

This XML markup must include the opening <b>Object</b> and closing <b>/Object</b> tags.

The encoding of the markup contained in <i>xmlMarkup</i> will be inferred. Inclusion of a <a href="https://msdn.microsoft.com/library/ms776429(v=VS.85).aspx">byte order mark</a> at the beginning of the buffer passed in <i>xmlMarkup</i> is optional.

The following encodings and <a href="https://msdn.microsoft.com/library/ms776429(v=VS.85).aspx">byte order mark</a> values are supported:<table>
<tr>
<th>Encoding</th>
<th>Description</th>
<th>Byte order mark</th>
</tr>
<tr>
<td>UTF8</td>
<td>UTF-8</td>
<td>EF BB BF</td>
</tr>
<tr>
<td>UTF16LE</td>
<td>UTF-16, little endian</td>
<td>FF FE</td>
</tr>
<tr>
<td>UTF16BE</td>
<td>UTF-16, big endian</td>
<td>FE FF</td>
</tr>
</table>
 




### -param count [in]

The size of the <i>xmlMarkup</i> buffer.


### -param customObject [out, retval]

A new <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer that represents the application-specific <b>Object</b> element.

This parameter can be <b>NULL</b> if a pointer to the  new interface is not needed.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>count</i> parameter is 0. The <i>xmlMarkup</i> parameter must be passed valid XML markup.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>xmlMarkup</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



An <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer provides access to the XML markup of the <b>Object</b> element it represents. To access the XML markup of the  <b>Object</b> element, call the <a href="https://msdn.microsoft.com/fedb6f47-59b9-4959-91ef-db1fb398aca9">IOpcSignatureCustomObject::GetXml</a> method.

When an <a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a> interface pointer is created and added to the set, the <b>Object</b>  it represents is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

