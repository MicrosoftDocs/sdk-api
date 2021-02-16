---
UID: NF:msopc.IOpcSigningOptions.GetCustomReferenceSet
title: IOpcSigningOptions::GetCustomReferenceSet (msopc.h)
description: Gets an IOpcSignatureReferenceSet interface pointer.
helpviewer_keywords: ["GetCustomReferenceSet","GetCustomReferenceSet method [Open Packaging Conventions]","GetCustomReferenceSet method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetCustomReferenceSet method","IOpcSigningOptions.GetCustomReferenceSet","IOpcSigningOptions::GetCustomReferenceSet","msopc/IOpcSigningOptions::GetCustomReferenceSet","opc.iopcsigningoptions_getcustomreferenceset"]
old-location: opc\iopcsigningoptions_getcustomreferenceset.htm
tech.root: OPC
ms.assetid: 2222772a-e396-4d78-a7e4-a12f19ec689b
ms.date: 12/05/2018
ms.keywords: GetCustomReferenceSet, GetCustomReferenceSet method [Open Packaging Conventions], GetCustomReferenceSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetCustomReferenceSet method, IOpcSigningOptions.GetCustomReferenceSet, IOpcSigningOptions::GetCustomReferenceSet, msopc/IOpcSigningOptions::GetCustomReferenceSet, opc.iopcsigningoptions_getcustomreferenceset
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
 - IOpcSigningOptions::GetCustomReferenceSet
 - msopc/IOpcSigningOptions::GetCustomReferenceSet
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
 - IOpcSigningOptions.GetCustomReferenceSet
---

# IOpcSigningOptions::GetCustomReferenceSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface pointer.

## -parameters

### -param customReferenceSet [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a>.

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
The <i>customReferenceSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereferenceset">IOpcSignatureReferenceSet</a> interface pointer that provides methods enabling the creation and deletion of the  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers in the set. The <b>IOpcSignatureReference</b> interface pointers represent references to XML elements to be signed.


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