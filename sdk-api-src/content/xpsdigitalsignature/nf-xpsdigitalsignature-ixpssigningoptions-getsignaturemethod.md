---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignatureMethod
title: IXpsSigningOptions::GetSignatureMethod (xpsdigitalsignature.h)
description: Gets the signature method.helpviewer_keywords: ["GetSignatureMethod","GetSignatureMethod method [XPS Documents and Packaging]","GetSignatureMethod method [XPS Documents and Packaging]","IXpsSigningOptions interface","IXpsSigningOptions interface [XPS Documents and Packaging]","GetSignatureMethod method","IXpsSigningOptions.GetSignatureMethod","IXpsSigningOptions::GetSignatureMethod","xps.ixpssigningoptions_getsignaturemethod","xpsdigitalsignature/IXpsSigningOptions::GetSignatureMethod"]
old-location: xps\ixpssigningoptions_getsignaturemethod.htm
tech.root: printdocs
ms.assetid: ab01420f-c401-463a-a695-4594c1f579d3
ms.date: 12/05/2018
ms.keywords: GetSignatureMethod, GetSignatureMethod method [XPS Documents and Packaging], GetSignatureMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignatureMethod method, IXpsSigningOptions.GetSignatureMethod, IXpsSigningOptions::GetSignatureMethod, xps.ixpssigningoptions_getsignaturemethod, xpsdigitalsignature/IXpsSigningOptions::GetSignatureMethod
f1_keywords:
- xpsdigitalsignature/IXpsSigningOptions.GetSignatureMethod
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsdigitalsignature.h
api_name:
- IXpsSigningOptions.GetSignatureMethod
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::GetSignatureMethod


## -description


Gets the signature method.


## -parameters




### -param signatureMethod [out, retval]

The signature method that is expressed as a URI. If no signature method has been set, a <b>NULL</b> pointer is returned.

The following signature methods have been tested in Windows 7:


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A signature method must be set before signing.

When a new instance of this interface is returned by <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not valid; they must be initialized before the new interface can be used as a parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign">Sign</a> method.

This method allocates the memory used by the string that is returned in <i>signatureMethod</i>.  If <i>signatureMethod</i> is not <b>NULL</b>, use the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Cryptography Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions">IXpsSigningOptions</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

