---
UID: NF:msopc.IOpcSignatureCustomObjectSet.Delete
title: IOpcSignatureCustomObjectSet::Delete (msopc.h)
description: Deletes a specified IOpcSignatureCustomObject interface pointer from the set.
helpviewer_keywords: ["Delete","Delete method [Open Packaging Conventions]","Delete method [Open Packaging Conventions]","IOpcSignatureCustomObjectSet interface","IOpcSignatureCustomObjectSet interface [Open Packaging Conventions]","Delete method","IOpcSignatureCustomObjectSet.Delete","IOpcSignatureCustomObjectSet::Delete","msopc/IOpcSignatureCustomObjectSet::Delete","opc.iopcsignaturecustomobjectset_delete"]
old-location: opc\iopcsignaturecustomobjectset_delete.htm
tech.root: OPC
ms.assetid: 7cfd8439-8f7e-4112-a2c0-3827922fb4b0
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Open Packaging Conventions], Delete method [Open Packaging Conventions],IOpcSignatureCustomObjectSet interface, IOpcSignatureCustomObjectSet interface [Open Packaging Conventions],Delete method, IOpcSignatureCustomObjectSet.Delete, IOpcSignatureCustomObjectSet::Delete, msopc/IOpcSignatureCustomObjectSet::Delete, opc.iopcsignaturecustomobjectset_delete
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
 - IOpcSignatureCustomObjectSet::Delete
 - msopc/IOpcSignatureCustomObjectSet::Delete
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
 - IOpcSignatureCustomObjectSet.Delete
---

# IOpcSignatureCustomObjectSet::Delete


## -description

Deletes a specified <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer from the set.

## -parameters

### -param customObject [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer to be deleted.

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
The <i>customObject</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer is deleted from the set, the <b>Object</b> it represents is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>