---
UID: NF:wmsecure.IWMSecureChannel.WMSC_GetValidCertificate
title: IWMSecureChannel::WMSC_GetValidCertificate (wmsecure.h)
description: The WMSC_GetValidCertificate method returns a copy of the certificate that was used provided by the other side of the connection. Also returns the index of the signature that validated that certificate.
helpviewer_keywords: ["IWMSecureChannel interface [windows Media Format]","WMSC_GetValidCertificate method","IWMSecureChannel.WMSC_GetValidCertificate","IWMSecureChannel::WMSC_GetValidCertificate","WMSC_GetValidCertificate","WMSC_GetValidCertificate method [windows Media Format]","WMSC_GetValidCertificate method [windows Media Format]","IWMSecureChannel interface","wmformat.iwmsecurechannel_wmsc_getvalidcertificate","wmsecure/IWMSecureChannel::WMSC_GetValidCertificate"]
old-location: wmformat\iwmsecurechannel_wmsc_getvalidcertificate.htm
tech.root: wmformat
ms.assetid: 0ecc25c5-238e-4415-952e-7d830ba1c317
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_GetValidCertificate method, IWMSecureChannel.WMSC_GetValidCertificate, IWMSecureChannel::WMSC_GetValidCertificate, WMSC_GetValidCertificate, WMSC_GetValidCertificate method [windows Media Format], WMSC_GetValidCertificate method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_getvalidcertificate, wmsecure/IWMSecureChannel::WMSC_GetValidCertificate
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IWMSecureChannel::WMSC_GetValidCertificate
 - wmsecure/IWMSecureChannel::WMSC_GetValidCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel.WMSC_GetValidCertificate
---

# IWMSecureChannel::WMSC_GetValidCertificate


## -description

<p class="CCE_Message">[<b>WMSC_GetValidCertificate</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>WMSC_GetValidCertificate</b> method returns a copy of the certificate that was used provided by the other side
     of the connection.   Also returns the index of the signature that validated
     that certificate.

## -parameters

### -param ppbCertificate [out]

<i>ppbCertificate</i> must be released with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> by the user.
     <i>ppbCertificate</i> can be <b>NULL</b> if no certificate was provided. 
     If no connection was made, this function returns E_FAIL

### -param pdwSignature [out]

<i>pdwSignature</i> can be 0xFFFFFFFF if no signature was used to validate the cert.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>