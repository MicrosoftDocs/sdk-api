---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCertificateSet
title: IXpsSigningOptions::GetCertificateSet (xpsdigitalsignature.h)
description: Gets an IOpcCertificateSet interface, which can be used to add additional certificates to the signature.
helpviewer_keywords: ["GetCertificateSet","GetCertificateSet method [XPS Documents and Packaging]","GetCertificateSet method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetCertificateSet method","IXpsSigningOptions.GetCertificateSet","IXpsSigningOptions::GetCertificateSet","xps.ixpssigningoptions_getcertificateset","xpsdigitalsignature/IXpsSigningOptions::GetCertificateSet"]
old-location: xps\ixpssigningoptions_getcertificateset.htm
tech.root: xps
ms.assetid: 40e96263-03dd-4fbe-8383-0c0bf1abd8c4
ms.date: 12/05/2018
ms.keywords: GetCertificateSet, GetCertificateSet method [XPS Documents and Packaging], GetCertificateSet method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCertificateSet method, IXpsSigningOptions.GetCertificateSet, IXpsSigningOptions::GetCertificateSet, xps.ixpssigningoptions_getcertificateset, xpsdigitalsignature/IXpsSigningOptions::GetCertificateSet
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - IXpsSigningOptions::GetCertificateSet
 - xpsdigitalsignature/IXpsSigningOptions::GetCertificateSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.GetCertificateSet
---

# IXpsSigningOptions::GetCertificateSet


## -description

Gets an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface, which can be used to add additional certificates to the signature.

## -parameters

### -param certificateSet [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a> interface.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this  method is optional and provides a way for an application to add  a signing certificate to the signature. The extra certificates in this set will be separate from   the signing certificate.

## -see-also

<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset">IOpcCertificateSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>