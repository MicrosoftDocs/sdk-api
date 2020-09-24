---
UID: NF:wintrust.WTHelperCertCheckValidSignature
title: WTHelperCertCheckValidSignature function (wintrust.h)
description: Checks whether a signature is valid.
helpviewer_keywords: ["WTHelperCertCheckValidSignature","WTHelperCertCheckValidSignature function [Security]","security.wthelpercertcheckvalidsignature","wintrust/WTHelperCertCheckValidSignature"]
old-location: security\wthelpercertcheckvalidsignature.htm
tech.root: security
ms.assetid: d46eea18-03cb-4199-873e-0e9e13061598
ms.date: 12/05/2018
ms.keywords: WTHelperCertCheckValidSignature, WTHelperCertCheckValidSignature function [Security], security.wthelpercertcheckvalidsignature, wintrust/WTHelperCertCheckValidSignature
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
 - WTHelperCertCheckValidSignature
 - wintrust/WTHelperCertCheckValidSignature
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
 - WTHelperCertCheckValidSignature
---

# WTHelperCertCheckValidSignature function


## -description

<p class="CCE_Message">[The <b>WTHelperCertCheckValidSignature</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperCertCheckValidSignature</b> function checks whether a signature is valid.  It can be used by trust providers to get an initial assessment of the validity of a signature before calling the function pointed to by the <b>pfnFinalPolicy</b> member of a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_functions">CRYPT_PROVIDER_FUNCTIONS</a> structure.

## -parameters

### -param pProvData

A pointer to the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure that contains the signer and countersigner information.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of possible error values, see <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a>.