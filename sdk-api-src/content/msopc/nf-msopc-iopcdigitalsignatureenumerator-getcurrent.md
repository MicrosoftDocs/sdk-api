---
UID: NF:msopc.IOpcDigitalSignatureEnumerator.GetCurrent
title: IOpcDigitalSignatureEnumerator::GetCurrent (msopc.h)
description: Gets the IOpcDigitalSignature interface pointer at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [Open Packaging Conventions]","GetCurrent method [Open Packaging Conventions]","IOpcDigitalSignatureEnumerator interface","IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions]","GetCurrent method","IOpcDigitalSignatureEnumerator.GetCurrent","IOpcDigitalSignatureEnumerator::GetCurrent","msopc/IOpcDigitalSignatureEnumerator::GetCurrent","opc.iopcdigitalsignatureenumerator_getcurrent"]
old-location: opc\iopcdigitalsignatureenumerator_getcurrent.htm
tech.root: OPC
ms.assetid: 2e211822-9fd8-424c-bd0c-c5c81f9abc0b
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcDigitalSignatureEnumerator interface, IOpcDigitalSignatureEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcDigitalSignatureEnumerator.GetCurrent, IOpcDigitalSignatureEnumerator::GetCurrent, msopc/IOpcDigitalSignatureEnumerator::GetCurrent, opc.iopcdigitalsignatureenumerator_getcurrent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpcDigitalSignatureEnumerator::GetCurrent
 - msopc/IOpcDigitalSignatureEnumerator::GetCurrent
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
 - IOpcDigitalSignatureEnumerator.GetCurrent
---

# IOpcDigitalSignatureEnumerator::GetCurrent


## -description

Gets the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointer at the current position of the enumerator.

## -parameters

### -param digitalSignature [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface pointer.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>partReference</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_DUPLICATE_PACKAGE_OBJECT_REFERENCES</b></dt>
<dt>0x8051002D</dt>
</dl>
</td>
<td width="60%">
The signature markup contains more than one <b>Reference</b> element that refers to the package <b>Object</b> element, but only one such <b>Reference</b> is allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_DUPLICATE_SIGNATURE_PROPERTY_ELEMENT</b></dt>
<dt>0x80510028</dt>
</dl>
</td>
<td width="60%">
The signature markup contains more than one <b>SignatureProperty</b> element that has the same <b>Id</b> attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_EXTERNAL_SIGNATURE_REFERENCE</b></dt>
<dt>0x8051002F</dt>
</dl>
</td>
<td width="60%">
A <b>Reference</b> element in the signature markup indicates an object that is external to the package. <b>Reference</b> elements must point to parts or <b>Object</b> elements that are internal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_CANONICALIZATION_METHOD</b></dt>
<dt>0x80510022</dt>
</dl>
</td>
<td width="60%">
An unsupported canonicalization method was requested or used in a signature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_SIGNATURE_COUNT</b></dt>
<dt>0x8051002B</dt>
</dl>
</td>
<td width="60%">
A Signature part does not contain the signature markup for exactly one signature.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_SIGNATURE_XML</b></dt>
<dt>0x8051002A</dt>
</dl>
</td>
<td width="60%">
The signature markup in a Signature part does not conform to the schema specified in the <i>OPC</i> or <a href="https://www.w3.org/TR/xmldsig-core/">XML-Signature Syntax and Processing</a> (http://www.w3.org/TR/xmldsig-core/).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_CANONICALIZATION_TRANSFORM</b></dt>
<dt>0x80510032</dt>
</dl>
</td>
<td width="60%">
A relationships transform must be followed by a canonicalization method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_PACKAGE_OBJECT_REFERENCE</b></dt>
<dt>0x8051002E</dt>
</dl>
</td>
<td width="60%">
The signature markup is missing a <b>Reference</b> to the package-specific  <b>Object</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_ALGORITHM</b></dt>
<dt>0x8051002C</dt>
</dl>
</td>
<td width="60%">
The signature markup does not specify signature method algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_PART</b></dt>
<dt>0x80510020</dt>
</dl>
</td>
<td width="60%">
The specified Signature part does not exist in the package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_PROPERTIES_ELEMENT</b></dt>
<dt>0x80510026</dt>
</dl>
</td>
<td width="60%">
The <b>SignatureProperties </b> element was not found in the signature markup.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_PROPERTY_ELEMENT</b></dt>
<dt>0x80510027</dt>
</dl>
</td>
<td width="60%">
The <b>SignatureProperty</b> child element of the <b>SignatureProperties</b> element was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MISSING_SIGNATURE_TIME_PROPERTY</b></dt>
<dt>0x80510029</dt>
</dl>
</td>
<td width="60%">
The <b>SignatureProperty</b>  element with the <b>Id</b> attribute value of "idSignatureTime" does not exist or is not correctly constructed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_MULTIPLE_RELATIONSHIP_TRANSFORMS</b></dt>
<dt>0x80510031</dt>
</dl>
</td>
<td width="60%">
More than one relationships transform is specified for a <b>Reference</b> element, but only one relationships transform  is allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_REFERENCE_MISSING_CONTENT_TYPE</b></dt>
<dt>0x80510030</dt>
</dl>
</td>
<td width="60%">
The <b>URI</b> attribute value of a <b>Reference</b> element in the signature markup does not include the content type of the referenced part.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_REFERENCE_MISSING_URI</b></dt>
<dt>0x80510043</dt>
</dl>
</td>
<td width="60%">
The <b>URI</b> attribute is required for a <b>Reference</b> element but is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_UNEXPECTED_CONTENT_TYPE</b></dt>
<dt>0x80510005</dt>
</dl>
</td>
<td width="60%">
Either the content type of a part differed from the expected content type (specified in the OPC, <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 Part 2</a>), or the part content did not match the part's  content type.

</td>
</tr>
</table>

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignatureenumerator-movenext">MoveNext</a> method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignatureenumerator">IOpcDigitalSignatureEnumerator</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>