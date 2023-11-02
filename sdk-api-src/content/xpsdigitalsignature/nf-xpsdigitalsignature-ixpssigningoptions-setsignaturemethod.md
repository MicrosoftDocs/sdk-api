---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignatureMethod
title: IXpsSigningOptions::SetSignatureMethod (xpsdigitalsignature.h)
description: Sets the signature method.
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetSignatureMethod method","IXpsSigningOptions.SetSignatureMethod","IXpsSigningOptions::SetSignatureMethod","SetSignatureMethod","SetSignatureMethod method [XPS Documents and Packaging]","SetSignatureMethod method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setsignaturemethod","xpsdigitalsignature/IXpsSigningOptions::SetSignatureMethod"]
old-location: xps\ixpssigningoptions_setsignaturemethod.htm
tech.root: xps
ms.assetid: 318f0e08-2384-4fab-a181-6ff3070ea21f
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignatureMethod method, IXpsSigningOptions.SetSignatureMethod, IXpsSigningOptions::SetSignatureMethod, SetSignatureMethod, SetSignatureMethod method [XPS Documents and Packaging], SetSignatureMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignaturemethod, xpsdigitalsignature/IXpsSigningOptions::SetSignatureMethod
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
 - IXpsSigningOptions::SetSignatureMethod
 - xpsdigitalsignature/IXpsSigningOptions::SetSignatureMethod
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
 - IXpsSigningOptions.SetSignatureMethod
---

# IXpsSigningOptions::SetSignatureMethod


## -description

Sets the signature method.

## -parameters

### -param signatureMethod [in]

The signature method expressed as a URI.

This parameter must refer to a valid signature method. The following signature methods have been tested in Windows 7:

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The signature method must be set before signing.

When a new instance of this interface is returned by <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not initialized; they must be initialized before the new interface can be used as a parameter of the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

The URI in  <i>signatureMethod</i>  must be the URI of a valid signing algorithm, such as http://www.w3.org/2000/09/xmldsig#rsa-sha1, and it must be
    supported by the signing certificate.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Cryptography Functions</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>