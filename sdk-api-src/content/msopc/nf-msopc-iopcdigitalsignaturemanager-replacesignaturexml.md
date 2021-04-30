---
UID: NF:msopc.IOpcDigitalSignatureManager.ReplaceSignatureXml
title: IOpcDigitalSignatureManager::ReplaceSignatureXml (msopc.h)
description: Replaces the existing signature markup that is stored in a specified signature part.
helpviewer_keywords: ["IOpcDigitalSignatureManager interface [Open Packaging Conventions]","ReplaceSignatureXml method","IOpcDigitalSignatureManager.ReplaceSignatureXml","IOpcDigitalSignatureManager::ReplaceSignatureXml","ReplaceSignatureXml","ReplaceSignatureXml method [Open Packaging Conventions]","ReplaceSignatureXml method [Open Packaging Conventions]","IOpcDigitalSignatureManager interface","msopc/IOpcDigitalSignatureManager::ReplaceSignatureXml","opc.iopcdigitalsignaturemanager_replacesignaturexml"]
old-location: opc\iopcdigitalsignaturemanager_replacesignaturexml.htm
tech.root: OPC
ms.assetid: cacd0ccf-0cb9-41dc-a944-74db8254fd95
ms.date: 12/05/2018
ms.keywords: IOpcDigitalSignatureManager interface [Open Packaging Conventions],ReplaceSignatureXml method, IOpcDigitalSignatureManager.ReplaceSignatureXml, IOpcDigitalSignatureManager::ReplaceSignatureXml, ReplaceSignatureXml, ReplaceSignatureXml method [Open Packaging Conventions], ReplaceSignatureXml method [Open Packaging Conventions],IOpcDigitalSignatureManager interface, msopc/IOpcDigitalSignatureManager::ReplaceSignatureXml, opc.iopcdigitalsignaturemanager_replacesignaturexml
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
 - IOpcDigitalSignatureManager::ReplaceSignatureXml
 - msopc/IOpcDigitalSignatureManager::ReplaceSignatureXml
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
 - IOpcDigitalSignatureManager.ReplaceSignatureXml
---

# IOpcDigitalSignatureManager::ReplaceSignatureXml


## -description

Replaces the existing signature markup that is stored in a specified signature part.

## -parameters

### -param signaturePartName [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the signature part that stores the existing signature markup.

### -param newSignatureXml [in]

A buffer that contains the signature markup that will replace the existing markup.

### -param count [in]

The size of the <i>newSignatureXml</i> buffer.

### -param digitalSignature [out, retval]

A pointer to a new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a> interface that represents the signature derived from the signature markup that is passed in <i>newSignatureXml</i>.

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
At least one of the <i>signaturePartName</i>, <i>newSignatureXml</i>, and <i>digitalSignature</i> parameters is <b>NULL</b>.
              

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
The <i>newSignatureXml</i> buffer contains more than one <b>Reference</b> element that refers to the package <b>Object</b> element, but only one such <b>Reference</b> is allowed.

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
The <i>newSignatureXml</i> buffer contains more than one <b>SignatureProperty</b> element that has the same <b>Id</b> attribute.

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
In the <i>newSignatureXml</i> buffer, a <b>Reference</b> element refers to an object that is external to the package. <b>Reference</b> elements must point to parts or <b>Object</b> elements that are internal.

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
 An unsupported canonicalization method was requested or used in the <i>newSignatureXml</i> buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_INVALID_RELATIONSHIP_TRANSFORM_XML</b></dt>
<dt>0x80510021</dt>
</dl>
</td>
<td width="60%">
In the <i>newSignatureXml</i> buffer, a <b>Transform</b> element that indicates the use of the relationships transform and  the selection criteria for the transform does not conform to the schema specified in the <i>OPC</i>.

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
The <i>newSignatureXml</i> buffer  does not contain the signature markup for exactly one signature.

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
The size of the <i>newSignatureXml</i> buffer is 0,  but this buffer must have a size that is greater than 0.

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
In the <i>newSignatureXml</i> buffer, a relationships transform is not followed by a canonicalization method; the relationships transform must be followed by a canonicalization method.

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
In the <i>newSignatureXml</i> buffer,  a <b>Reference</b> to the package-specific  <b>Object</b> element was not found.

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
The signature markup in the <i>newSignatureXml</i> buffer does not specify a signature method algorithm.

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
In the <i>newSignatureXml</i> buffer, the <b>SignatureProperties </b> element was not found.

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
In the <i>newSignatureXml</i> buffer, the <b>SignatureProperty</b> child element of the <b>SignatureProperties</b> element was not found.

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
In the <i>newSignatureXml</i> buffer, the <b>SignatureProperty</b>  element with the <b>Id</b> attribute value of "idSignatureTime" does not exist or is not correctly constructed.

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
In the <i>newSignatureXml</i> buffer,  more than one relationships transform is specified for a <b>Reference</b> element, but only one relationships transform  is allowed.

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
The <b>URI</b> attribute value of a <b>Reference</b> element in the <i>newSignatureXml</i> buffer does not include the content type of the referenced part.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_SIGNATURE_PROPERTY_MISSING_TARGET</b></dt>
<dt>0x80510045</dt>
</dl>
</td>
<td width="60%">
In the <i>newSignatureXml</i> buffer, the <b>SignatureProperty</b> element is missing the required <b>Target</b> attribute.

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
A <b>Reference</b> element, which is in the <i>newSignatureXml</i> buffer, requires the <b>URI</b> attribute, but the attribute is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_UNSIGNED_PACKAGE</b></dt>
<dt>0x80510055</dt>
</dl>
</td>
<td width="60%">
The package is not signed; therefore, the signature markup cannot be replaced. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_PART</b></dt>
<dt>0x80510018</dt>
</dl>
</td>
<td width="60%">
The specified part does not exist.

</td>
</tr>
</table>

## -remarks

This method does not validate the signature that is derived from the  new signature markup that is in the <i>newSignatureXml</i> parameter.
      
        

The caller must confirm that the new signature markup, which replaces the existing signature markup in the specified signature part, will not break the signature.
      

This method changes the existing signature markup; certificates and relationships that have the specified signature part as their source are preserved.
      


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>