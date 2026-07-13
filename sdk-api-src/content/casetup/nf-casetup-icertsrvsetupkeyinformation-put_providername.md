---
UID: NF:casetup.ICertSrvSetupKeyInformation.put_ProviderName
title: ICertSrvSetupKeyInformation::put_ProviderName (casetup.h)
description: Gets or sets the name of the cryptographic service provider (CSP) or key storage provider (KSP) that is used to generate or store the private key. (Put)
helpviewer_keywords: ["ICertSrvSetupKeyInformation interface [Security]","ProviderName property","ICertSrvSetupKeyInformation.ProviderName","ICertSrvSetupKeyInformation.put_ProviderName","ICertSrvSetupKeyInformation::ProviderName","ICertSrvSetupKeyInformation::get_ProviderName","ICertSrvSetupKeyInformation::put_ProviderName","ProviderName property [Security]","ProviderName property [Security]","ICertSrvSetupKeyInformation interface","casetup/ICertSrvSetupKeyInformation::ProviderName","casetup/ICertSrvSetupKeyInformation::get_ProviderName","casetup/ICertSrvSetupKeyInformation::put_ProviderName","put_ProviderName","security.icertsrvsetupkeyinformation_providername"]
old-location: security\icertsrvsetupkeyinformation_providername.htm
tech.root: security
ms.assetid: a8f50b34-0403-40c0-9ecb-f663ccbd622a
ms.date: 12/05/2018
ms.keywords: ICertSrvSetupKeyInformation interface [Security],ProviderName property, ICertSrvSetupKeyInformation.ProviderName, ICertSrvSetupKeyInformation.put_ProviderName, ICertSrvSetupKeyInformation::ProviderName, ICertSrvSetupKeyInformation::get_ProviderName, ICertSrvSetupKeyInformation::put_ProviderName, ProviderName property [Security], ProviderName property [Security],ICertSrvSetupKeyInformation interface, casetup/ICertSrvSetupKeyInformation::ProviderName, casetup/ICertSrvSetupKeyInformation::get_ProviderName, casetup/ICertSrvSetupKeyInformation::put_ProviderName, put_ProviderName, security.icertsrvsetupkeyinformation_providername
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
 - ICertSrvSetupKeyInformation::put_ProviderName
 - casetup/ICertSrvSetupKeyInformation::put_ProviderName
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
 - ICertSrvSetupKeyInformation.ProviderName
 - ICertSrvSetupKeyInformation.get_ProviderName
 - ICertSrvSetupKeyInformation.put_ProviderName
---

# ICertSrvSetupKeyInformation::put_ProviderName


## -description

The <b>ProviderName</b> property gets or sets the name of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) or <a href="/windows/desktop/SecGloss/k-gly">key storage provider</a> (KSP) that is used to generate or store the <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

This property is read/write.

## -parameters

## -remarks

For a KSP, the <b>ProviderName</b> property value must be formatted as <i>PublicKeyAlgorithmName</i>, number sign (#), and <i>KeyStorageProviderName</i>, for example "RSA#Microsoft Software Key Storage Provider" or "ECDSA_P256#Microsoft Software Key Storage Provider". The <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a> must be supported by the provider. To get supported algorithms, call the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptenumalgorithms">NCryptEnumAlgorithms</a> function with the <i>dwAlgOperations</i> parameter set to <b>NCRYPT_SIGNATURE_OPERATION</b>. For information about algorithm identifiers, see <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a>
