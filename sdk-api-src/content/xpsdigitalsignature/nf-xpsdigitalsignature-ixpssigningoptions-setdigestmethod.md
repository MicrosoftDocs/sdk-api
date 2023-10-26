---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetDigestMethod
title: IXpsSigningOptions::SetDigestMethod (xpsdigitalsignature.h)
description: Sets the URI of the digest method.
helpviewer_keywords: ["IXpsSigningOptions interface [XPS Documents and Packaging]","SetDigestMethod method","IXpsSigningOptions.SetDigestMethod","IXpsSigningOptions::SetDigestMethod","SetDigestMethod","SetDigestMethod method [XPS Documents and Packaging]","SetDigestMethod method [XPS Documents and Packaging]","IXpsSigningOptions interface","xps.ixpssigningoptions_setdigestmethod","xpsdigitalsignature/IXpsSigningOptions::SetDigestMethod"]
old-location: xps\ixpssigningoptions_setdigestmethod.htm
tech.root: xps
ms.assetid: d9f72cc4-38b2-4a91-8813-183483d47986
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetDigestMethod method, IXpsSigningOptions.SetDigestMethod, IXpsSigningOptions::SetDigestMethod, SetDigestMethod, SetDigestMethod method [XPS Documents and Packaging], SetDigestMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setdigestmethod, xpsdigitalsignature/IXpsSigningOptions::SetDigestMethod
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
 - IXpsSigningOptions::SetDigestMethod
 - xpsdigitalsignature/IXpsSigningOptions::SetDigestMethod
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
 - IXpsSigningOptions.SetDigestMethod
---

# IXpsSigningOptions::SetDigestMethod


## -description

Sets the URI of the digest method.

## -parameters

### -param digestMethod [in]

The URI of the digest method.

This parameter must refer to the URI of a valid digest method. The following digest methods have been tested in Windows 7:

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The digest method must be set before signing.

When a new instance of this interface is returned by <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not initialized. They must be initialized before the new interface can be used as a parameter of the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

Sets the string  that identifies the URI of the algorithm that is used to digest the parts, relationships, and signature references. The following is an example of a valid URI:   <a href="http://www.w3.org/2000/09/xmldsig">http://www.w3.org/2000/09/xmldsig#sha1</a>.

The signing certificate, signature method, 
    and digest method must be compatible with one another.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Cryptography Functions</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>