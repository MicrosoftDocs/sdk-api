---
UID: NF:msopc.IOpcSigningOptions.GetCertificateEmbeddingOption
title: IOpcSigningOptions::GetCertificateEmbeddingOption (msopc.h)
description: Gets a value that specifies the storage location in the package of the certificate to be used for the signature.
helpviewer_keywords: ["GetCertificateEmbeddingOption","GetCertificateEmbeddingOption method [Open Packaging Conventions]","GetCertificateEmbeddingOption method [Open Packaging Conventions]","IOpcSigningOptions interface","IOpcSigningOptions interface [Open Packaging Conventions]","GetCertificateEmbeddingOption method","IOpcSigningOptions.GetCertificateEmbeddingOption","IOpcSigningOptions::GetCertificateEmbeddingOption","msopc/IOpcSigningOptions::GetCertificateEmbeddingOption","opc.iopcsigningoptions_getcertificateembeddingoption"]
old-location: opc\iopcsigningoptions_getcertificateembeddingoption.htm
tech.root: OPC
ms.assetid: 86f83829-0507-4918-ae7f-71738f985068
ms.date: 12/05/2018
ms.keywords: GetCertificateEmbeddingOption, GetCertificateEmbeddingOption method [Open Packaging Conventions], GetCertificateEmbeddingOption method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetCertificateEmbeddingOption method, IOpcSigningOptions.GetCertificateEmbeddingOption, IOpcSigningOptions::GetCertificateEmbeddingOption, msopc/IOpcSigningOptions::GetCertificateEmbeddingOption, opc.iopcsigningoptions_getcertificateembeddingoption
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
 - IOpcSigningOptions::GetCertificateEmbeddingOption
 - msopc/IOpcSigningOptions::GetCertificateEmbeddingOption
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
 - IOpcSigningOptions.GetCertificateEmbeddingOption
---

# IOpcSigningOptions::GetCertificateEmbeddingOption


## -description

Gets a value that specifies the storage location in the package of the certificate to be used for the signature.

## -parameters

### -param embeddingOption [out, retval]

A value that specifies the location of the certificate.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>embeddingOption</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_certificate_embedding_option">OPC_CERTIFICATE_EMBEDDING_OPTION</a> enum value.

</td>
</tr>
</table>

## -remarks

The default location of the certificate is <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>. To change this value, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-setcertificateembeddingoption">IOpcSigningOptions::SetCertificateEmbeddingOption</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_certificate_embedding_option">OPC_CERTIFICATE_EMBEDDING_OPTION</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>