---
UID: NF:msopc.IOpcSignatureReferenceSet.Create
title: IOpcSignatureReferenceSet::Create (msopc.h)
description: Creates an IOpcSignatureReference interface pointer that represents a reference to an XML element to be signed.
helpviewer_keywords: ["Create","Create method [Open Packaging Conventions]","Create method [Open Packaging Conventions]","IOpcSignatureReferenceSet interface","IOpcSignatureReferenceSet interface [Open Packaging Conventions]","Create method","IOpcSignatureReferenceSet.Create","IOpcSignatureReferenceSet::Create","msopc/IOpcSignatureReferenceSet::Create","opc.iopcsignaturereferenceset_create"]
old-location: opc\iopcsignaturereferenceset_create.htm
tech.root: OPC
ms.assetid: 5e943769-a043-4354-80e7-d471a1dbde7a
ms.date: 12/05/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignatureReferenceSet interface, IOpcSignatureReferenceSet interface [Open Packaging Conventions],Create method, IOpcSignatureReferenceSet.Create, IOpcSignatureReferenceSet::Create, msopc/IOpcSignatureReferenceSet::Create, opc.iopcsignaturereferenceset_create
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
 - IOpcSignatureReferenceSet::Create
 - msopc/IOpcSignatureReferenceSet::Create
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
 - IOpcSignatureReferenceSet.Create
---

# IOpcSignatureReferenceSet::Create


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer that represents a reference to an XML element to be signed.

## -parameters

### -param referenceUri [in]

The URI of  the referenced XML element.

Set the value of this parameter to a URI that represents "#" followed by  the <b>Id</b> attribute value of the referenced element: "#<i>&lt;elementIdValue&gt;</i>".

For examples, see the Remarks section.

### -param referenceId [in]

The <b>Id</b> attribute of the <b>Reference</b> element that represents the reference in signature  markup. To omit the  <b>Id</b> attribute, set this parameter value to  <b>NULL</b>.

### -param type [in]

The <b>Type</b> attribute of the <b>Reference</b> element that represents the reference in signature markup. To omit the <b>Type</b> attribute, set this parameter value to  <b>NULL</b>.

### -param digestMethod [in]

The digest method to be used for the XML markup to be referenced. To use the default digest method,  set this parameter value to  <b>NULL</b>.

<div class="alert"><b>Important</b>  The default digest method must be set by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">IOpcSigningOptions::SetDefaultDigestMethod</a> method before <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> is called.</div>
<div> </div>

### -param transformMethod [in]

The canonicalization method to be used for the XML markup to be referenced.

### -param reference [out, retval]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer that represents the reference to  the XML element to be signed.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>transformMethod</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>referenceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DS_PACKAGE_REFERENCE_URI_RESERVED</b></dt>
<dt>0x80510025</dt>
</dl>
</td>
<td width="60%">
The reserved <b>URI</b> attribute value of the signature's <b>Reference</b> element to the package <b>Object</b> is being used as the <b>URI</b> attribute value of a <b>Reference</b> to a custom <b>Object</b> element.

</td>
</tr>
</table>

## -remarks

This method creates a reference to an XML element that is signed when the signature is generated. The referenced element can be either an application-specific <b>Object</b> element or a child of an application-specific <b>Object</b>.

To reference an XML element for signing, set the <i>referenceUri</i> parameter value to a URI that represents "#" followed by  the <b>Id</b> attribute value of the referenced element, as shown in the following table.<table>
<tr>
<th><i>referenceUri</i> Value as String</th>
<th>Referenced Element</th>
<th>Element Description</th>
</tr>
<tr>
<td>"#<i>idMyCustomObject</i>"</td>
<td>"&lt;Object Id="<i>idMyCustomObject</i>"&gt;<i>...</i>&lt;/Object&gt;"</td>
<td>
An application-specific <b>Object</b> element.

</td>
</tr>
<tr>
<td>"#<i>idMyElement</i>"</td>
<td>"&lt;Object&gt;&lt;<i>MyElement</i> Id="<i>idMyElement</i>"&gt;<i>...</i>&lt;/<i>MyElement</i>&gt;...&lt;/Object&gt;"</td>
<td>
A child element of an application-specific <b>Object</b>.

</td>
</tr>
</table>
 



This method does not create the reference to the package-specific <b>Object</b> element to be signed; that reference is created automatically when the signature is generated.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>