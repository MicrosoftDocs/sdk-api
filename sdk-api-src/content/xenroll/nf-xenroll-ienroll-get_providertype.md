---
UID: NF:xenroll.IEnroll.get_ProviderType
title: IEnroll::get_ProviderType (xenroll.h)
description: Sets or retrieves the type of provider.
old-location: security\ienroll4_providertype.htm
tech.root: SecCrypto
ms.assetid: d4ab2b0e-127f-4ec0-9e4a-4314561912e3
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],ProviderType property, IEnroll.ProviderType, IEnroll.get_ProviderType, IEnroll::ProviderType, IEnroll::get_ProviderType, IEnroll::put_ProviderType, ProviderType property [Security], ProviderType property [Security],IEnroll interface, get_ProviderType, security.ienroll4_providertype, xenroll/IEnroll::ProviderType, xenroll/IEnroll::get_ProviderType, xenroll/IEnroll::put_ProviderType
f1_keywords:
- xenroll/IEnroll.ProviderType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Xenroll.dll
api_name:
- IEnroll.ProviderType
- IEnroll.get_ProviderType
- IEnroll.put_ProviderType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll::get_ProviderType


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderType</b> property sets or retrieves the type of provider.

The value of the <b>ProviderType</b> property is passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use. The default value for this property is 1. This property was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For general information about provider types, see 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptographic-provider-types">Cryptographic Provider Types</a>.

For more information about valid values for the Microsoft Base Cryptographic Provider, see the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function.

For provider type information for other CSPs, see the documentation provided with the CSP.

The <b>ProviderType</b> property value is passed to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  by using its <i>dwProvType</i> parameter.


The <b>ProviderType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr">enumProvidersWStr</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
 

 

