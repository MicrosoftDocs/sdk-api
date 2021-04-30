---
UID: NF:wincrypt.CertVerifyTimeValidity
title: CertVerifyTimeValidity function (wincrypt.h)
description: The CertVerifyTimeValidity function verifies the time validity of a certificate.
helpviewer_keywords: ["CertVerifyTimeValidity","CertVerifyTimeValidity function [Security]","_crypto2_certverifytimevalidity","security.certverifytimevalidity","wincrypt/CertVerifyTimeValidity"]
old-location: security\certverifytimevalidity.htm
tech.root: security
ms.assetid: 9ccf9230-e998-4f82-9db0-6cbaa1c36850
ms.date: 12/05/2018
ms.keywords: CertVerifyTimeValidity, CertVerifyTimeValidity function [Security], _crypto2_certverifytimevalidity, security.certverifytimevalidity, wincrypt/CertVerifyTimeValidity
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertVerifyTimeValidity
 - wincrypt/CertVerifyTimeValidity
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
 - CertVerifyTimeValidity
---

# CertVerifyTimeValidity function


## -description

The <b>CertVerifyTimeValidity</b> function verifies the time validity of a certificate.

## -parameters

### -param pTimeToVerify [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the comparison time. If <b>NULL</b>, the current time is used.

### -param pCertInfo [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure of the certificate for which the time is being verified.

## -returns

Returns a minus one if the comparison time is before the <b>NotBefore</b> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure. Returns a plus one if the comparison time is after the <b>NotAfter</b> member. Returns zero for valid time for the certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrlrevocation">CertVerifyCRLRevocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrltimevalidity">CertVerifyCRLTimeValidity</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyvaliditynesting">CertVerifyValidityNesting</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>