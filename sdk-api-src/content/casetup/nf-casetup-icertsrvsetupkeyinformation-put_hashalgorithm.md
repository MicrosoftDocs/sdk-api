---
UID: NF:casetup.ICertSrvSetupKeyInformation.put_HashAlgorithm
title: ICertSrvSetupKeyInformation::put_HashAlgorithm (casetup.h)
description: Gets or sets the name of the hashing algorithm used to sign or verify the certification authority (CA) certificate for the key. (Put)
helpviewer_keywords: ["HashAlgorithm property [Security]","HashAlgorithm property [Security]","ICertSrvSetupKeyInformation interface","ICertSrvSetupKeyInformation interface [Security]","HashAlgorithm property","ICertSrvSetupKeyInformation.HashAlgorithm","ICertSrvSetupKeyInformation.put_HashAlgorithm","ICertSrvSetupKeyInformation::HashAlgorithm","ICertSrvSetupKeyInformation::get_HashAlgorithm","ICertSrvSetupKeyInformation::put_HashAlgorithm","casetup/ICertSrvSetupKeyInformation::HashAlgorithm","casetup/ICertSrvSetupKeyInformation::get_HashAlgorithm","casetup/ICertSrvSetupKeyInformation::put_HashAlgorithm","put_HashAlgorithm","security.icertsrvsetupkeyinformation_hashalgorithm"]
old-location: security\icertsrvsetupkeyinformation_hashalgorithm.htm
tech.root: security
ms.assetid: f1e007d1-eadb-4ab6-91bc-3c8a61b54aca
ms.date: 12/05/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],ICertSrvSetupKeyInformation interface, ICertSrvSetupKeyInformation interface [Security],HashAlgorithm property, ICertSrvSetupKeyInformation.HashAlgorithm, ICertSrvSetupKeyInformation.put_HashAlgorithm, ICertSrvSetupKeyInformation::HashAlgorithm, ICertSrvSetupKeyInformation::get_HashAlgorithm, ICertSrvSetupKeyInformation::put_HashAlgorithm, casetup/ICertSrvSetupKeyInformation::HashAlgorithm, casetup/ICertSrvSetupKeyInformation::get_HashAlgorithm, casetup/ICertSrvSetupKeyInformation::put_HashAlgorithm, put_HashAlgorithm, security.icertsrvsetupkeyinformation_hashalgorithm
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetupKeyInformation::put_HashAlgorithm
 - casetup/ICertSrvSetupKeyInformation::put_HashAlgorithm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetupKeyInformation.HashAlgorithm
 - ICertSrvSetupKeyInformation.get_HashAlgorithm
 - ICertSrvSetupKeyInformation.put_HashAlgorithm
---

# ICertSrvSetupKeyInformation::put_HashAlgorithm


## -description

The <b>HashAlgorithm</b> property gets or sets the name of the <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> used to  sign or verify the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate for the key.

This property is read/write.

## -parameters

## -remarks

The hashing algorithm must be supported by the <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername">ProviderName</a> provider. For <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs), get supported algorithms by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function for the given provider. For <a href="/windows/desktop/SecGloss/k-gly">key storage providers</a> (KSPs), get supported algorithms by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumalgorithms">BCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>BCRYPT_HASH_OPERATION</b>. For information about algorithm identifiers, see <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a>.


#### Examples

For an example of enumerating supported algorithms by using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a>, see <a href="/windows/desktop/SecCrypto/example-c-program-enumerating-csp-providers-and-provider-types">Example C Program: Enumerating CSP Providers and Provider Types</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a>
