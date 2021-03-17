---
UID: NF:msopc.IOpcSignaturePartReference.GetPartName
title: IOpcSignaturePartReference::GetPartName (msopc.h)
description: Gets the part name of the referenced part.
helpviewer_keywords: ["GetPartName","GetPartName method [Open Packaging Conventions]","GetPartName method [Open Packaging Conventions]","IOpcSignaturePartReference interface","IOpcSignaturePartReference interface [Open Packaging Conventions]","GetPartName method","IOpcSignaturePartReference.GetPartName","IOpcSignaturePartReference::GetPartName","msopc/IOpcSignaturePartReference::GetPartName","opc.iopcsignaturepartreference_getpartname"]
old-location: opc\iopcsignaturepartreference_getpartname.htm
tech.root: OPC
ms.assetid: bf34361f-da74-4785-8e5b-8b9caf809a41
ms.date: 12/05/2018
ms.keywords: GetPartName, GetPartName method [Open Packaging Conventions], GetPartName method [Open Packaging Conventions],IOpcSignaturePartReference interface, IOpcSignaturePartReference interface [Open Packaging Conventions],GetPartName method, IOpcSignaturePartReference.GetPartName, IOpcSignaturePartReference::GetPartName, msopc/IOpcSignaturePartReference::GetPartName, opc.iopcsignaturepartreference_getpartname
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
 - IOpcSignaturePartReference::GetPartName
 - msopc/IOpcSignaturePartReference::GetPartName
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
 - IOpcSignaturePartReference.GetPartName
---

# IOpcSignaturePartReference::GetPartName


## -description

Gets the part name of the referenced part.

## -parameters

### -param partName [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface that represents the part name.

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
The <i>partName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>