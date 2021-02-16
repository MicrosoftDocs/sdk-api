---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureId
title: IOpcDigitalSignature::GetSignatureId (msopc.h)
description: Gets the value of the Id attribute from the Signature element of the signature markup.
helpviewer_keywords: ["GetSignatureId","GetSignatureId method [Open Packaging Conventions]","GetSignatureId method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignatureId method","IOpcDigitalSignature.GetSignatureId","IOpcDigitalSignature::GetSignatureId","msopc/IOpcDigitalSignature::GetSignatureId","opc.iopcdigitalsignature_getsignatureid"]
old-location: opc\iopcdigitalsignature_getsignatureid.htm
tech.root: OPC
ms.assetid: 20eea0ff-dff1-4f95-aaf7-00e5a36503f1
ms.date: 12/05/2018
ms.keywords: GetSignatureId, GetSignatureId method [Open Packaging Conventions], GetSignatureId method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureId method, IOpcDigitalSignature.GetSignatureId, IOpcDigitalSignature::GetSignatureId, msopc/IOpcDigitalSignature::GetSignatureId, opc.iopcdigitalsignature_getsignatureid
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
 - IOpcDigitalSignature::GetSignatureId
 - msopc/IOpcDigitalSignature::GetSignatureId
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
 - IOpcDigitalSignature.GetSignatureId
---

# IOpcDigitalSignature::GetSignatureId


## -description

Gets the value of the <b>Id</b> attribute from the <b>Signature</b> element of the signature markup.

## -parameters

### -param signatureId [out, retval]

A pointer to the <b>Id</b> attribute value of the signature markup <b>Signature</b> element.

If the <b>Signature</b> element does not have an <b>Id</b> attribute value, <i>signatureId</i> will be the empty string.

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
The <i>signatureId</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates memory used by the string returned in <i>signatureId</i>.  If the method succeeds, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

The <b>Id</b> attribute of the <b>Signature</b> element is optional. If this method is not called, the <b>Signature</b> element will not have the <b>Id</b> attribute.

To set the signature Id before the signature is generated, call  the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setsignatureid">IOpcSigningOptions::SetSignatureId</a> method.

To access the Id before the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignatureid">IOpcSigningOptions::GetSignatureId</a>. method.

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