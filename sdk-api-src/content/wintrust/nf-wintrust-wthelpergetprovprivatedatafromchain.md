---
UID: NF:wintrust.WTHelperGetProvPrivateDataFromChain
title: WTHelperGetProvPrivateDataFromChain function (wintrust.h)
description: Receives a CRYPT_PROVIDER_PRIVDATA structure from the chain by using the provider ID.
helpviewer_keywords: ["WTHelperGetProvPrivateDataFromChain","WTHelperGetProvPrivateDataFromChain function [Security]","security.wthelpergetprovprivatedatafromchain","wintrust/WTHelperGetProvPrivateDataFromChain"]
old-location: security\wthelpergetprovprivatedatafromchain.htm
tech.root: security
ms.assetid: 67a718a2-47ca-4c45-a939-99dd8311dc6d
ms.date: 12/05/2018
ms.keywords: WTHelperGetProvPrivateDataFromChain, WTHelperGetProvPrivateDataFromChain function [Security], security.wthelpergetprovprivatedatafromchain, wintrust/WTHelperGetProvPrivateDataFromChain
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
 - WTHelperGetProvPrivateDataFromChain
 - wintrust/WTHelperGetProvPrivateDataFromChain
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
 - WTHelperGetProvPrivateDataFromChain
---

# WTHelperGetProvPrivateDataFromChain function


## -description

<p class="CCE_Message">[The <b>WTHelperGetProvPrivateDataFromChain</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperGetProvPrivateDataFromChain</b> function receives a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_privdata">CRYPT_PROVIDER_PRIVDATA</a> structure from the chain by using the provider ID. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param pProvData [in]

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure that contains the provider's private information.

### -param pgProviderID

A pointer to a <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the provider.

## -returns

If the function succeeds, the function returns a pointer to a  <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_privdata">CRYPT_PROVIDER_PRIVDATA</a> structure that represents the trust provider's private information.

If the function fails, the return value is <b>NULL</b>.