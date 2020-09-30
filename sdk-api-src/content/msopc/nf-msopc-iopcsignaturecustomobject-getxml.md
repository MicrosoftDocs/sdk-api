---
UID: NF:msopc.IOpcSignatureCustomObject.GetXml
title: IOpcSignatureCustomObject::GetXml (msopc.h)
description: Gets the XML markup of an application-specific Object element.
helpviewer_keywords: ["GetXml","GetXml method [Open Packaging Conventions]","GetXml method [Open Packaging Conventions]","IOpcSignatureCustomObject interface","IOpcSignatureCustomObject interface [Open Packaging Conventions]","GetXml method","IOpcSignatureCustomObject.GetXml","IOpcSignatureCustomObject::GetXml","msopc/IOpcSignatureCustomObject::GetXml","opc.iopcsignaturecustomobject_getxml"]
old-location: opc\iopcsignaturecustomobject_getxml.htm
tech.root: OPC
ms.assetid: fedb6f47-59b9-4959-91ef-db1fb398aca9
ms.date: 12/05/2018
ms.keywords: GetXml, GetXml method [Open Packaging Conventions], GetXml method [Open Packaging Conventions],IOpcSignatureCustomObject interface, IOpcSignatureCustomObject interface [Open Packaging Conventions],GetXml method, IOpcSignatureCustomObject.GetXml, IOpcSignatureCustomObject::GetXml, msopc/IOpcSignatureCustomObject::GetXml, opc.iopcsignaturecustomobject_getxml
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcSignatureCustomObject::GetXml
 - msopc/IOpcSignatureCustomObject::GetXml
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureCustomObject.GetXml
---

# IOpcSignatureCustomObject::GetXml


## -description

Gets the XML markup of an application-specific <b>Object</b> element.

## -parameters

### -param xmlMarkup [out]

A pointer to a buffer that contains the XML markup of an <b>Object</b> element and includes the opening and closing <b>Object</b> tags.

In the buffer, XML markup is preceded by a <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a> that corresponds to the encoding of the markup.

Supported encodings and <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a> values.<table>
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
 



For an example of a buffer with a <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a>, see the Remarks section.

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

This method allocates memory used by the buffer returned in <i>xmlMarkup</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

Serialized application-specific <b>Object</b> elements in signature markup can be added, removed, or modified by replacing the signature markup.

To replace signature markup, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-replacesignaturexml">IOpcDigitalSignatureManager::ReplaceSignatureXml</a> method. The caller must ensure that addition, deletion, or modification of application-specific <b>Object</b> elements does not break the signature.

To sign an application-specific  <b>Object</b> element or a child of that element, create a reference to the XML element to be signed. Create the reference by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">IOpcSignatureReferenceSet::Create</a> method with the <i>referenceUri</i> parameter value set to "#" followed by the <b>Id</b> attribute value  of the referenced element. For example, if the <b>Id</b> attribute of the referenced element is "Application",  set <i>referenceUri</i> to "#Application".

The following table shows a <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a> at the beginning of an <i>xmlMarkup</i> buffer that contains "&lt;Object Id="id1"&gt;&lt;/Object&gt;":
		

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

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>