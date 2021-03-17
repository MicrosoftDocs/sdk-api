---
UID: NF:msopc.IOpcSigningOptions.GetSignaturePartReferenceSet
title: IOpcSigningOptions::GetSignaturePartReferenceSet (msopc.h)
description: Gets an IOpcSignaturePartReferenceSet interface.
helpviewer_keywords: ["GetSignaturePartReferenceSet","GetSignaturePartReferenceSet method [Open Packaging Conventions]","GetSignaturePartReferenceSet method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetSignaturePartReferenceSet method","IOpcSigningOptions.GetSignaturePartReferenceSet","IOpcSigningOptions::GetSignaturePartReferenceSet","msopc/IOpcSigningOptions::GetSignaturePartReferenceSet","opc.iopcsigningoptions_getsignaturepartreferenceset"]
old-location: opc\iopcsigningoptions_getsignaturepartreferenceset.htm
tech.root: OPC
ms.assetid: 60e657c3-41a3-4a05-a084-111429b1add9
ms.date: 12/05/2018
ms.keywords: GetSignaturePartReferenceSet, GetSignaturePartReferenceSet method [Open Packaging Conventions], GetSignaturePartReferenceSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignaturePartReferenceSet method, IOpcSigningOptions.GetSignaturePartReferenceSet, IOpcSigningOptions::GetSignaturePartReferenceSet, msopc/IOpcSigningOptions::GetSignaturePartReferenceSet, opc.iopcsigningoptions_getsignaturepartreferenceset
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
 - IOpcSigningOptions::GetSignaturePartReferenceSet
 - msopc/IOpcSigningOptions::GetSignaturePartReferenceSet
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
 - IOpcSigningOptions.GetSignaturePartReferenceSet
---

# IOpcSigningOptions::GetSignaturePartReferenceSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a> interface.

## -parameters

### -param partReferenceSet [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a> interface pointers.

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
The <i>partReferenceSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a> interface pointer that provides methods enabling the creation and deletion of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers in the set. The <b>IOpcSignaturePartReference</b> interface pointers represent references to parts to be signed. 


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