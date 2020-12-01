---
UID: NF:msopc.IOpcSigningOptions.SetCertificateEmbeddingOption
title: IOpcSigningOptions::SetCertificateEmbeddingOption (msopc.h)
description: Set the storage location of the certificate to be used for the signature.
helpviewer_keywords: ["IOpcSigningOptions interface [Open Packaging Conventions]","SetCertificateEmbeddingOption method","IOpcSigningOptions.SetCertificateEmbeddingOption","IOpcSigningOptions::SetCertificateEmbeddingOption","SetCertificateEmbeddingOption","SetCertificateEmbeddingOption method [Open Packaging Conventions]","SetCertificateEmbeddingOption method [Open Packaging Conventions]","IOpcSigningOptions interface","msopc/IOpcSigningOptions::SetCertificateEmbeddingOption","opc.iopcsigningoptions_setcertificateembeddingoption"]
old-location: opc\iopcsigningoptions_setcertificateembeddingoption.htm
tech.root: OPC
ms.assetid: afae4b98-c05f-4fa3-bb1e-f9f43ee86e64
ms.date: 12/05/2018
ms.keywords: IOpcSigningOptions interface [Open Packaging Conventions],SetCertificateEmbeddingOption method, IOpcSigningOptions.SetCertificateEmbeddingOption, IOpcSigningOptions::SetCertificateEmbeddingOption, SetCertificateEmbeddingOption, SetCertificateEmbeddingOption method [Open Packaging Conventions], SetCertificateEmbeddingOption method [Open Packaging Conventions],IOpcSigningOptions interface, msopc/IOpcSigningOptions::SetCertificateEmbeddingOption, opc.iopcsigningoptions_setcertificateembeddingoption
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
 - IOpcSigningOptions::SetCertificateEmbeddingOption
 - msopc/IOpcSigningOptions::SetCertificateEmbeddingOption
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
 - IOpcSigningOptions.SetCertificateEmbeddingOption
---

# IOpcSigningOptions::SetCertificateEmbeddingOption


## -description

Set the storage location of the certificate to be used for the signature.

## -parameters

### -param embeddingOption [in]

The <a href="/windows/win32/api/msopc/ne-msopc-opc_certificate_embedding_option">OPC_CERTIFICATE_EMBEDDING_OPTION</a> value that describes the location of the certificate.

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
The <i>embeddingOption</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method changes the location of the certificate from the default location, <b>OPC_CERTIFICATE_IN_CERTIFICATE_PART</b>, to a location that is specified by the caller.

To access the value that describes the certificate location, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcertificateembeddingoption">IOpcSigningOptions::GetCertificateEmbeddingOption</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignaturemanager">IOpcDigitalSignatureManager</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>