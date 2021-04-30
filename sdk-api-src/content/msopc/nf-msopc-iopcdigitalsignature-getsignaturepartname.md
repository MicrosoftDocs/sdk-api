---
UID: NF:msopc.IOpcDigitalSignature.GetSignaturePartName
title: IOpcDigitalSignature::GetSignaturePartName (msopc.h)
description: Gets the part name of the part that contains the signature markup.
helpviewer_keywords: ["GetSignaturePartName","GetSignaturePartName method [Open Packaging Conventions]","GetSignaturePartName method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignaturePartName method","IOpcDigitalSignature.GetSignaturePartName","IOpcDigitalSignature::GetSignaturePartName","msopc/IOpcDigitalSignature::GetSignaturePartName","opc.iopcdigitalsignature_getsignaturepartname"]
old-location: opc\iopcdigitalsignature_getsignaturepartname.htm
tech.root: OPC
ms.assetid: 0a7f9413-d44d-4d3d-bb4e-01ef14ee7a1c
ms.date: 12/05/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [Open Packaging Conventions], GetSignaturePartName method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignaturePartName method, IOpcDigitalSignature.GetSignaturePartName, IOpcDigitalSignature::GetSignaturePartName, msopc/IOpcDigitalSignature::GetSignaturePartName, opc.iopcdigitalsignature_getsignaturepartname
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
 - IOpcDigitalSignature::GetSignaturePartName
 - msopc/IOpcDigitalSignature::GetSignaturePartName
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
 - IOpcDigitalSignature.GetSignaturePartName
---

# IOpcDigitalSignature::GetSignaturePartName


## -description

Gets the part name of the part that contains the signature markup.

## -parameters

### -param signaturePartName [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface pointer that represents the part name of the signature part that contains the signature markup.

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
The <i>signaturePartName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To set the part name of this signature part before the signature is generated, call  the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignaturepartname">IOpcSigningOptions::SetSignaturePartName</a> method. To access the signature part name before the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturepartname">IOpcSigningOptions::GetSignaturePartName</a>.

The signature part that stores signature markup is specific to the signature.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>