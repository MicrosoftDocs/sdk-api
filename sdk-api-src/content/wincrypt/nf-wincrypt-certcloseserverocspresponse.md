---
UID: NF:wincrypt.CertCloseServerOcspResponse
title: CertCloseServerOcspResponse function (wincrypt.h)
description: Closes an online certificate status protocol (OCSP) server response handle.
helpviewer_keywords: ["CertCloseServerOcspResponse","CertCloseServerOcspResponse function [Security]","security.certcloseserverocspresponse","wincrypt/CertCloseServerOcspResponse"]
old-location: security\certcloseserverocspresponse.htm
tech.root: security
ms.assetid: 6247e8ca-ba12-432f-9bf8-a6c644f253e9
ms.date: 12/05/2018
ms.keywords: CertCloseServerOcspResponse, CertCloseServerOcspResponse function [Security], security.certcloseserverocspresponse, wincrypt/CertCloseServerOcspResponse
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertCloseServerOcspResponse
 - wincrypt/CertCloseServerOcspResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCloseServerOcspResponse
---

# CertCloseServerOcspResponse function


## -description

The <b>CertCloseServerOcspResponse</b> function closes an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) server response handle.

## -parameters

### -param hServerOcspResponse [in]

The handle to close for an OCSP server response.

### -param dwFlags [in]

This parameter is not used and must be zero.

## -remarks

The <b>CertCloseServerOcspResponse</b> function closes a handle returned by either the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddrefserverocspresponse">CertAddRefServerOcspResponse</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenserverocspresponse">CertOpenServerOcspResponse</a>