---
UID: NF:msopc.IOpcSignatureCustomObject.GetXml
title: IOpcSignatureCustomObject::GetXml
author: windows-sdk-content
description: Gets the XML markup of an application-specific Object element.
old-location: opc\iopcsignaturecustomobject_getxml.htm
tech.root: OPC
ms.assetid: fedb6f47-59b9-4959-91ef-db1fb398aca9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetXml, GetXml method [Open Packaging Conventions], GetXml method [Open Packaging Conventions],IOpcSignatureCustomObject interface, IOpcSignatureCustomObject interface [Open Packaging Conventions],GetXml method, IOpcSignatureCustomObject.GetXml, IOpcSignatureCustomObject::GetXml, msopc/IOpcSignatureCustomObject::GetXml, opc.iopcsignaturecustomobject_getxml
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
 - IOpcSignatureCustomObject.GetXml
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureCustomObject::GetXml


## -description


Gets the XML markup of an application-specific <b>Object</b> element.


## -parameters




### -param xmlMarkup [out]

A pointer to a buffer that contains the XML markup of an <b>Object</b> element and includes the opening and closing <b>Object</b> tags.

In the buffer, XML markup is preceded by a <a href="_win32_Byte_Order_Mark">byte order mark</a> that corresponds to the encoding of the markup.

Supported encodings and <a href="_win32_Byte_Order_Mark">byte order mark</a> values.<table>
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
 



For an example of a buffer with a <a href="_win32_Byte_Order_Mark">byte order mark</a>, see the Remarks section.


### -param count [out]

A pointer to  the size of the <i>xmlMarkup</i> buffer.


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
 At least one of the <i>xmlMarkup</i>, and <i>count</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the buffer returned in <i>xmlMarkup</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.

Serialized application-specific <b>Object</b> elements in signature markup can be added, removed, or modified by replacing the signature markup.

To replace signature markup, call the <a href="https://msdn.microsoft.com/cacd0ccf-0cb9-41dc-a944-74db8254fd95">IOpcDigitalSignatureManager::ReplaceSignatureXml</a> method. The caller must ensure that addition, deletion, or modification of application-specific <b>Object</b> elements does not break the signature.

To sign an application-specific  <b>Object</b> element or a child of that element, create a reference to the XML element to be signed. Create the reference by calling the <a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">IOpcSignatureReferenceSet::Create</a> method with the <i>referenceUri</i> parameter value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application",  set <i>referenceUri</i> to "#Application".

The following table shows a <a href="_win32_Byte_Order_Mark">byte order mark</a> at the beginning of an <i>xmlMarkup</i> buffer that contains "&lt;Object Id="id1"&gt;&lt;/Object&gt;":
		

<table>
<tr>
<th>Buffer Byte Index</th>
<td>0</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
<td>7</td>
<td>...</td>
</tr>
<tr>
<th>UTF8 Value</th>
<td>EF</td>
<td>BB</td>
<td>BF</td>
<td>'&lt;'</td>
<td>'O'</td>
<td>'b'</td>
<td>'j'</td>
<td>'e'</td>
<td>...</td>
</tr>
<tr>
<th>UTF16LE Value</th>
<td>FF</td>
<td>FE</td>
<td>'&lt;'</td>
<td>00</td>
<td>'O'</td>
<td>00</td>
<td>'b'</td>
<td>00</td>
<td>...</td>
</tr>
</table>
 


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/4ebb4fbe-66cc-46d9-b548-31177d9f6da9">IOpcSignatureCustomObject</a>



<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

