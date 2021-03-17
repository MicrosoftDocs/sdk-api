---
UID: NF:wintrust.WTHelperGetProvSignerFromChain
title: WTHelperGetProvSignerFromChain function (wintrust.h)
description: Retrieves a signer or countersigner by index from the chain.
helpviewer_keywords: ["WTHelperGetProvSignerFromChain","WTHelperGetProvSignerFromChain function [Security]","security.wthelpergetprovsignerfromchain","wintrust/WTHelperGetProvSignerFromChain"]
old-location: security\wthelpergetprovsignerfromchain.htm
tech.root: security
ms.assetid: 8e1ebf82-73c2-445b-9964-6739f7c90c47
ms.date: 12/05/2018
ms.keywords: WTHelperGetProvSignerFromChain, WTHelperGetProvSignerFromChain function [Security], security.wthelpergetprovsignerfromchain, wintrust/WTHelperGetProvSignerFromChain
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
 - WTHelperGetProvSignerFromChain
 - wintrust/WTHelperGetProvSignerFromChain
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
 - WTHelperGetProvSignerFromChain
---

# WTHelperGetProvSignerFromChain function


## -description

<p class="CCE_Message">[The <b>WTHelperGetProvSignerFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperGetProvSignerFromChain</b> function retrieves a  signer or countersigner by index from the chain.  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param pProvData [in]

A pointer to the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure that contains the signer and countersigner information.

### -param idxSigner [in]

The index of the signer. The index is zero based.

### -param fCounterSigner [in]

If <b>TRUE</b>, the countersigner, as specified by <i>idxCounterSigner</i>, is retrieved by this function; the signer that contains the countersigner is identified by  <i>idxSigner</i>. If <b>FALSE</b>, the signer, as specified by <i>idxSigner</i>, is retrieved by this function.

### -param idxCounterSigner [in]

The index of the countersigner. The index is zero based. The countersigner applies to the signer identified by <i>idxSigner</i>.

## -returns

If the function succeeds, the function returns a pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_sgnr">CRYPT_PROVIDER_SGNR</a> structure for the requested signer or countersigner.

If the function fails, it returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wintrust/nf-wintrust-wthelpergetprovcertfromchain">WTHelperGetProvCertFromChain</a>