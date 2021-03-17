---
UID: NF:xenroll.IEnroll4.getCertContextFromFileResponseWStr
title: IEnroll4::getCertContextFromFileResponseWStr (xenroll.h)
description: Retrieves the certificate from a file containing a response from a certification authority.
helpviewer_keywords: ["IEnroll4 interface [Security]","getCertContextFromFileResponseWStr method","IEnroll4.getCertContextFromFileResponseWStr","IEnroll4::getCertContextFromFileResponseWStr","getCertContextFromFileResponseWStr","getCertContextFromFileResponseWStr method [Security]","getCertContextFromFileResponseWStr method [Security]","IEnroll4 interface","security.ienroll4_getcertcontextfromfileresponsewstr","xenroll/IEnroll4::getCertContextFromFileResponseWStr"]
old-location: security\ienroll4_getcertcontextfromfileresponsewstr.htm
tech.root: security
ms.assetid: 04a57bd4-4e04-41eb-97c9-87bfb51be645
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],getCertContextFromFileResponseWStr method, IEnroll4.getCertContextFromFileResponseWStr, IEnroll4::getCertContextFromFileResponseWStr, getCertContextFromFileResponseWStr, getCertContextFromFileResponseWStr method [Security], getCertContextFromFileResponseWStr method [Security],IEnroll4 interface, security.ienroll4_getcertcontextfromfileresponsewstr, xenroll/IEnroll4::getCertContextFromFileResponseWStr
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll4::getCertContextFromFileResponseWStr
 - xenroll/IEnroll4::getCertContextFromFileResponseWStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.getCertContextFromFileResponseWStr
---

# IEnroll4::getCertContextFromFileResponseWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertContextFromFileResponseWStr</b> method retrieves the certificate from a file containing a response from a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pwszResponseFileName [in]

A pointer to a null-terminated wide character string that represents the name of the file containing the response.

### -param ppCertContext [out]

A pointer to a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that receives the certificate retrieved from the response.

## -remarks

The response contained in <i>pwszResponseFileName</i> must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response. However, to accept a full CMC response, the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> must support <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>