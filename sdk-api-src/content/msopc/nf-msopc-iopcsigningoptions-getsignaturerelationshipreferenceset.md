---
UID: NF:msopc.IOpcSigningOptions.GetSignatureRelationshipReferenceSet
title: IOpcSigningOptions::GetSignatureRelationshipReferenceSet (msopc.h)
description: Gets an IOpcSignatureRelationshipReferenceSet interface pointer.
helpviewer_keywords: ["GetSignatureRelationshipReferenceSet","GetSignatureRelationshipReferenceSet method [Open Packaging Conventions]","GetSignatureRelationshipReferenceSet method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetSignatureRelationshipReferenceSet method","IOpcSigningOptions.GetSignatureRelationshipReferenceSet","IOpcSigningOptions::GetSignatureRelationshipReferenceSet","msopc/IOpcSigningOptions::GetSignatureRelationshipReferenceSet","opc.iopcsigningoptions_getsignaturerelationshipreferenceset"]
old-location: opc\iopcsigningoptions_getsignaturerelationshipreferenceset.htm
tech.root: OPC
ms.assetid: f89327d2-63ff-4b14-bde0-8fdf65f73e37
ms.date: 12/05/2018
ms.keywords: GetSignatureRelationshipReferenceSet, GetSignatureRelationshipReferenceSet method [Open Packaging Conventions], GetSignatureRelationshipReferenceSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignatureRelationshipReferenceSet method, IOpcSigningOptions.GetSignatureRelationshipReferenceSet, IOpcSigningOptions::GetSignatureRelationshipReferenceSet, msopc/IOpcSigningOptions::GetSignatureRelationshipReferenceSet, opc.iopcsigningoptions_getsignaturerelationshipreferenceset
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
 - IOpcSigningOptions::GetSignatureRelationshipReferenceSet
 - msopc/IOpcSigningOptions::GetSignatureRelationshipReferenceSet
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
 - IOpcSigningOptions.GetSignatureRelationshipReferenceSet
---

# IOpcSigningOptions::GetSignatureRelationshipReferenceSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a> interface pointer.

## -parameters

### -param relationshipReferenceSet [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a> interface pointer.

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
The <i>relationshipReferenceSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a> interface pointer that provides methods enabling the creation and deletion of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers in the set. The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers represent references to Relationships parts that contain relationships to be signed.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>