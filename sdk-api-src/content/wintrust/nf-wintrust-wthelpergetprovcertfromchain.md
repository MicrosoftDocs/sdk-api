---
UID: NF:wintrust.WTHelperGetProvCertFromChain
title: WTHelperGetProvCertFromChain function (wintrust.h)
description: Retrieves a trust provider certificate from the certificate chain.
helpviewer_keywords: ["WTHelperGetProvCertFromChain","WTHelperGetProvCertFromChain function [Security]","security.wthelpergetprovcertfromchain","wintrust/WTHelperGetProvCertFromChain"]
old-location: security\wthelpergetprovcertfromchain.htm
tech.root: security
ms.assetid: 047278fe-37d5-4fd6-8b36-9e28ead0cc5a
ms.date: 12/05/2018
ms.keywords: WTHelperGetProvCertFromChain, WTHelperGetProvCertFromChain function [Security], security.wthelpergetprovcertfromchain, wintrust/WTHelperGetProvCertFromChain
req.header: wintrust.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTHelperGetProvCertFromChain
 - wintrust/WTHelperGetProvCertFromChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WTHelperGetProvCertFromChain
---

# WTHelperGetProvCertFromChain function


## -description

<p class="CCE_Message">[The <b>WTHelperGetProvCertFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The  <b>WTHelperGetProvCertFromChain</b> function retrieves a trust provider certificate from the certificate chain.  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param pSgnr [in]

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_sgnr">CRYPT_PROVIDER_SGNR</a> structure that represents the signers. This pointer is retrieved by the <a href="/windows/desktop/api/wintrust/nf-wintrust-wthelpergetprovsignerfromchain">WTHelperGetProvSignerFromChain</a> function.

### -param idxCert [in]

The index of the certificate. The index is zero based.

## -returns

If the function succeeds, the function returns a pointer to a  <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_cert">CRYPT_PROVIDER_CERT</a> structure that represents the trust provider certificate.

If the function fails, it returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wintrust/nf-wintrust-wthelpergetprovsignerfromchain">WTHelperGetProvSignerFromChain</a>