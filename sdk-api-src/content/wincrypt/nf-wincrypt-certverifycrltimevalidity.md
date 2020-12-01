---
UID: NF:wincrypt.CertVerifyCRLTimeValidity
title: CertVerifyCRLTimeValidity function (wincrypt.h)
description: The CertVerifyCRLTimeValidity function verifies the time validity of a CRL.
helpviewer_keywords: ["CertVerifyCRLTimeValidity","CertVerifyCRLTimeValidity function [Security]","_crypto2_certverifycrltimevalidity","security.certverifycrltimevalidity","wincrypt/CertVerifyCRLTimeValidity"]
old-location: security\certverifycrltimevalidity.htm
tech.root: security
ms.assetid: ff321fe8-df45-4a1d-b626-055fb0696438
ms.date: 12/05/2018
ms.keywords: CertVerifyCRLTimeValidity, CertVerifyCRLTimeValidity function [Security], _crypto2_certverifycrltimevalidity, security.certverifycrltimevalidity, wincrypt/CertVerifyCRLTimeValidity
req.header: wincrypt.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertVerifyCRLTimeValidity
 - wincrypt/CertVerifyCRLTimeValidity
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
 - CertVerifyCRLTimeValidity
---

# CertVerifyCRLTimeValidity function


## -description

The <b>CertVerifyCRLTimeValidity</b> function verifies the time validity of a CRL.

## -parameters

### -param pTimeToVerify [in]

A pointer to <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure containing the time to be used in the verification. If set to <b>NULL</b>, the current time is used.

### -param pCrlInfo [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a> structure containing the CRL for which the time is to be verified.

## -returns

Returns a minus one (–1) if the comparison time is before the <b>ThisUpdate</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a> pointed to by <i>pCrlInfo</i>. Returns a plus one (+1) if the comparison time is after the <b>NextUpdate</b> time. Returns zero for valid time for the CRL.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrlrevocation">CertVerifyCRLRevocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifytimevalidity">CertVerifyTimeValidity</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyvaliditynesting">CertVerifyValidityNesting</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>