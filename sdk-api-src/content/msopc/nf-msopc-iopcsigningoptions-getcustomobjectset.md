---
UID: NF:msopc.IOpcSigningOptions.GetCustomObjectSet
title: IOpcSigningOptions::GetCustomObjectSet (msopc.h)
description: Gets an IOpcSignatureCustomObjectSet interface.
helpviewer_keywords: ["GetCustomObjectSet","GetCustomObjectSet method [Open Packaging Conventions]","GetCustomObjectSet method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetCustomObjectSet method","IOpcSigningOptions.GetCustomObjectSet","IOpcSigningOptions::GetCustomObjectSet","msopc/IOpcSigningOptions::GetCustomObjectSet","opc.iopcsigningoptions_getcustomobjectset"]
old-location: opc\iopcsigningoptions_getcustomobjectset.htm
tech.root: OPC
ms.assetid: 1b4d31cb-f12a-4b51-8b28-470e065e1661
ms.date: 12/05/2018
ms.keywords: GetCustomObjectSet, GetCustomObjectSet method [Open Packaging Conventions], GetCustomObjectSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetCustomObjectSet method, IOpcSigningOptions.GetCustomObjectSet, IOpcSigningOptions::GetCustomObjectSet, msopc/IOpcSigningOptions::GetCustomObjectSet, opc.iopcsigningoptions_getcustomobjectset
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
 - IOpcSigningOptions::GetCustomObjectSet
 - msopc/IOpcSigningOptions::GetCustomObjectSet
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
 - IOpcSigningOptions.GetCustomObjectSet
---

# IOpcSigningOptions::GetCustomObjectSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface.

## -parameters

### -param customObjectSet [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>.

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
The <i>customObjectSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a> interface pointer that provides methods enabling the creation and deletion of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers in the set. The <b>IOpcSignatureCustomObject</b> interface pointers represent application-specific <b>Object</b> elements which are serialized in the signature markup when the signature is generated.


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