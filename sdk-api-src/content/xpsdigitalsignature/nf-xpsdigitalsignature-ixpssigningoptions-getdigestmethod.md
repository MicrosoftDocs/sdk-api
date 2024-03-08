---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetDigestMethod
title: IXpsSigningOptions::GetDigestMethod (xpsdigitalsignature.h)
description: Gets the current digest method.
helpviewer_keywords: ["GetDigestMethod","GetDigestMethod method [XPS Documents and Packaging]","GetDigestMethod method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetDigestMethod method","IXpsSigningOptions.GetDigestMethod","IXpsSigningOptions::GetDigestMethod","xps.ixpssigningoptions_getdigestmethod","xpsdigitalsignature/IXpsSigningOptions::GetDigestMethod"]
old-location: xps\ixpssigningoptions_getdigestmethod.htm
tech.root: xps
ms.assetid: b8976719-970b-4598-8f1c-0ef2446ae12b
ms.date: 12/05/2018
ms.keywords: GetDigestMethod, GetDigestMethod method [XPS Documents and Packaging], GetDigestMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetDigestMethod method, IXpsSigningOptions.GetDigestMethod, IXpsSigningOptions::GetDigestMethod, xps.ixpssigningoptions_getdigestmethod, xpsdigitalsignature/IXpsSigningOptions::GetDigestMethod
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
 - IXpsSigningOptions::GetDigestMethod
 - xpsdigitalsignature/IXpsSigningOptions::GetDigestMethod
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
 - IXpsSigningOptions.GetDigestMethod
---

# IXpsSigningOptions::GetDigestMethod


## -description

Gets the current digest method.

## -parameters

### -param digestMethod [out, retval]

The current digest method.

The following digest methods have been tested in Windows 7:

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The digest method must be set before signing.

When a new instance of this interface is returned by <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not valid; they must be initialized before the new interface can be used as a parameter of the <a href="/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

This method allocates the memory used by the string that is returned in <i>digestMethod</i>.  If <i>digestMethod</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Cryptography Functions</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>