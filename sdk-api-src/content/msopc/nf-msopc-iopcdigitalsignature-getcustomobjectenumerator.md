---
UID: NF:msopc.IOpcDigitalSignature.GetCustomObjectEnumerator
title: IOpcDigitalSignature::GetCustomObjectEnumerator (msopc.h)
description: Gets an enumerator of IOpcSignatureCustomObject interface pointers that represent application-specific Object elements in the signature markup.
helpviewer_keywords: ["GetCustomObjectEnumerator","GetCustomObjectEnumerator method [Open Packaging Conventions]","GetCustomObjectEnumerator method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetCustomObjectEnumerator method","IOpcDigitalSignature.GetCustomObjectEnumerator","IOpcDigitalSignature::GetCustomObjectEnumerator","msopc/IOpcDigitalSignature::GetCustomObjectEnumerator","opc.iopcdigitalsignature_getcustomobjectenumerator"]
old-location: opc\iopcdigitalsignature_getcustomobjectenumerator.htm
tech.root: OPC
ms.assetid: 1263ca86-8b4f-4be9-a88a-f11e76178d0d
ms.date: 12/05/2018
ms.keywords: GetCustomObjectEnumerator, GetCustomObjectEnumerator method [Open Packaging Conventions], GetCustomObjectEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetCustomObjectEnumerator method, IOpcDigitalSignature.GetCustomObjectEnumerator, IOpcDigitalSignature::GetCustomObjectEnumerator, msopc/IOpcDigitalSignature::GetCustomObjectEnumerator, opc.iopcdigitalsignature_getcustomobjectenumerator
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
 - IOpcDigitalSignature::GetCustomObjectEnumerator
 - msopc/IOpcDigitalSignature::GetCustomObjectEnumerator
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
 - IOpcDigitalSignature.GetCustomObjectEnumerator
---

# IOpcDigitalSignature::GetCustomObjectEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers that represent application-specific <b>Object</b> elements in the signature markup.

## -parameters

### -param customObjectEnumerator [out, retval]

A pointer to an enumerator of  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointers.

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
The <i>customObjectEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectenumerator">IOpcSignatureCustomObjectEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>