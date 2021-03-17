---
UID: NF:msopc.IOpcSignaturePartReferenceSet.Create
title: IOpcSignaturePartReferenceSet::Create (msopc.h)
description: Creates an IOpcSignaturePartReference interface pointer that represents a reference to a part to be signed, and adds the new interface to the set.
helpviewer_keywords: ["Create","Create method [Open Packaging Conventions]","Create method [Open Packaging Conventions]","IOpcSignaturePartReferenceSet interface","IOpcSignaturePartReferenceSet interface [Open Packaging Conventions]","Create method","IOpcSignaturePartReferenceSet.Create","IOpcSignaturePartReferenceSet::Create","msopc/IOpcSignaturePartReferenceSet::Create","opc.iopcsignaturepartreferenceset_create"]
old-location: opc\iopcsignaturepartreferenceset_create.htm
tech.root: OPC
ms.assetid: 63162b37-0262-4d92-a14f-726fe4c87cc1
ms.date: 12/05/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignaturePartReferenceSet interface, IOpcSignaturePartReferenceSet interface [Open Packaging Conventions],Create method, IOpcSignaturePartReferenceSet.Create, IOpcSignaturePartReferenceSet::Create, msopc/IOpcSignaturePartReferenceSet::Create, opc.iopcsignaturepartreferenceset_create
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
 - IOpcSignaturePartReferenceSet::Create
 - msopc/IOpcSignaturePartReferenceSet::Create
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
 - IOpcSignaturePartReferenceSet.Create
---

# IOpcSignaturePartReferenceSet::Create


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer that represents a reference to a part to be signed, and adds the new interface to the set.

## -parameters

### -param partUri [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> that represents the part name of the part to be referenced.

### -param digestMethod [in]

The digest method to be used for part content of the part to be referenced. To use the default digest method, pass <b>NULL</b> to this parameter. <div class="alert"><b>Important</b>  The default digest method must be set by calling the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setdefaultdigestmethod">IOpcSigningOptions::SetDefaultDigestMethod</a> method before <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignaturemanager-sign">IOpcDigitalSignatureManager::Sign</a> is called.</div>
<div> </div>

### -param transformMethod [in]

The canonicalization method  used for part content of the part to be referenced.

### -param partReference [out, retval]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer that represents the reference to  the part to be signed.

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
The <i>partUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Only parts that can be represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface can be referenced by an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer. Relationships parts are referenced for signing  by a pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface. To create an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a> method.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>