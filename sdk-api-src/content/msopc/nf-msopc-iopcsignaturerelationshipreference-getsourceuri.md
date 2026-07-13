---
UID: NF:msopc.IOpcSignatureRelationshipReference.GetSourceUri
title: IOpcSignatureRelationshipReference::GetSourceUri (msopc.h)
description: Gets the source URI of the relationships that are stored in the referenced Relationships part.
helpviewer_keywords: ["GetSourceUri","GetSourceUri method [Open Packaging Conventions]","GetSourceUri method [Open Packaging Conventions]","IOpcSignatureRelationshipReference interface","IOpcSignatureRelationshipReference interface [Open Packaging Conventions]","GetSourceUri method","IOpcSignatureRelationshipReference.GetSourceUri","IOpcSignatureRelationshipReference::GetSourceUri","msopc/IOpcSignatureRelationshipReference::GetSourceUri","opc.iopcsignaturerelationshipreference_getsourceuri"]
old-location: opc\iopcsignaturerelationshipreference_getsourceuri.htm
tech.root: OPC
ms.assetid: d08cfbf0-0917-4ca4-85be-5ca62d7029d0
ms.date: 12/05/2018
ms.keywords: GetSourceUri, GetSourceUri method [Open Packaging Conventions], GetSourceUri method [Open Packaging Conventions],IOpcSignatureRelationshipReference interface, IOpcSignatureRelationshipReference interface [Open Packaging Conventions],GetSourceUri method, IOpcSignatureRelationshipReference.GetSourceUri, IOpcSignatureRelationshipReference::GetSourceUri, msopc/IOpcSignatureRelationshipReference::GetSourceUri, opc.iopcsignaturerelationshipreference_getsourceuri
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
 - IOpcSignatureRelationshipReference::GetSourceUri
 - msopc/IOpcSignatureRelationshipReference::GetSourceUri
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
 - IOpcSignatureRelationshipReference.GetSourceUri
---

# IOpcSignatureRelationshipReference::GetSourceUri


## -description

Gets the  source URI of the relationships that are stored in the referenced Relationships part.

## -parameters

### -param sourceUri [out, retval]

A pointer to the source URI of the relationships that are stored in the referenced Relationships part.

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
The <i>sourceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>