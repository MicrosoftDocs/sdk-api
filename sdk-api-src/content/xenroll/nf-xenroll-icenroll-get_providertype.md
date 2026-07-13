---
UID: NF:xenroll.ICEnroll.get_ProviderType
title: ICEnroll::get_ProviderType (xenroll.h)
description: The ProviderType property of ICEnroll4 sets or retrieves the type of provider. (Get)
helpviewer_keywords: ["CEnroll object [Security]","ProviderType property","ICEnroll interface [Security]","ProviderType property","ICEnroll.ProviderType","ICEnroll.get_ProviderType","ICEnroll2 interface [Security]","ProviderType property","ICEnroll2.ProviderType","ICEnroll2::get_ProviderType","ICEnroll2::put_ProviderType","ICEnroll3 interface [Security]","ProviderType property","ICEnroll3.ProviderType","ICEnroll3::get_ProviderType","ICEnroll3::put_ProviderType","ICEnroll4 interface [Security]","ProviderType property","ICEnroll4.ProviderType","ICEnroll4::ProviderType","ICEnroll4::get_ProviderType","ICEnroll4::put_ProviderType","ICEnroll::get_ProviderType","ICEnroll::put_ProviderType","ProviderType property [Security]","ProviderType property [Security]","CEnroll object","ProviderType property [Security]","ICEnroll interface","ProviderType property [Security]","ICEnroll2 interface","ProviderType property [Security]","ICEnroll3 interface","ProviderType property [Security]","ICEnroll4 interface","get_ProviderType","security.icenroll4_providertype","xenroll/ICEnroll2::ProviderType","xenroll/ICEnroll2::get_ProviderType","xenroll/ICEnroll2::put_ProviderType","xenroll/ICEnroll3::ProviderType","xenroll/ICEnroll3::get_ProviderType","xenroll/ICEnroll3::put_ProviderType","xenroll/ICEnroll4::ProviderType","xenroll/ICEnroll4::get_ProviderType","xenroll/ICEnroll4::put_ProviderType","xenroll/ICEnroll::ProviderType","xenroll/ICEnroll::get_ProviderType","xenroll/ICEnroll::put_ProviderType"]
old-location: security\icenroll4_providertype.htm
tech.root: security
ms.assetid: 90daa97a-350e-4307-80a5-b018cc1f0e86
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],ProviderType property, ICEnroll interface [Security],ProviderType property, ICEnroll.ProviderType, ICEnroll.get_ProviderType, ICEnroll2 interface [Security],ProviderType property, ICEnroll2.ProviderType, ICEnroll2::get_ProviderType, ICEnroll2::put_ProviderType, ICEnroll3 interface [Security],ProviderType property, ICEnroll3.ProviderType, ICEnroll3::get_ProviderType, ICEnroll3::put_ProviderType, ICEnroll4 interface [Security],ProviderType property, ICEnroll4.ProviderType, ICEnroll4::ProviderType, ICEnroll4::get_ProviderType, ICEnroll4::put_ProviderType, ICEnroll::get_ProviderType, ICEnroll::put_ProviderType, ProviderType property [Security], ProviderType property [Security],CEnroll object, ProviderType property [Security],ICEnroll interface, ProviderType property [Security],ICEnroll2 interface, ProviderType property [Security],ICEnroll3 interface, ProviderType property [Security],ICEnroll4 interface, get_ProviderType, security.icenroll4_providertype, xenroll/ICEnroll2::ProviderType, xenroll/ICEnroll2::get_ProviderType, xenroll/ICEnroll2::put_ProviderType, xenroll/ICEnroll3::ProviderType, xenroll/ICEnroll3::get_ProviderType, xenroll/ICEnroll3::put_ProviderType, xenroll/ICEnroll4::ProviderType, xenroll/ICEnroll4::get_ProviderType, xenroll/ICEnroll4::put_ProviderType, xenroll/ICEnroll::ProviderType, xenroll/ICEnroll::get_ProviderType, xenroll/ICEnroll::put_ProviderType
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
 - ICEnroll::get_ProviderType
 - xenroll/ICEnroll::get_ProviderType
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
 - ICEnroll4.ProviderType
 - ICEnroll4.get_ProviderType
 - ICEnroll4.put_ProviderType
 - ICEnroll3.ProviderType
 - ICEnroll3.get_ProviderType
 - ICEnroll3.put_ProviderType
 - ICEnroll2.ProviderType
 - ICEnroll2.get_ProviderType
 - ICEnroll2.put_ProviderType
 - ICEnroll.ProviderType
 - ICEnroll.get_ProviderType
 - ICEnroll.put_ProviderType
 - CEnroll.ProviderType
---

# ICEnroll::get_ProviderType


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderType</b> property sets or retrieves the type of provider.

The value of the <b>ProviderType</b> property is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use. The default value for this property is 1. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

For general information about provider types, see 
<a href="/windows/desktop/SecCrypto/cryptographic-provider-types">Cryptographic Provider Types</a>.

For more information about valid values for the Microsoft Base Cryptographic Provider, see the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function.

For provider type information for other CSPs, see the documentation provided with the CSP.

The <b>ProviderType</b> property value is passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  by using its <i>dwProvType</i> parameter.


The <b>ProviderType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-enumproviders">enumProviders</a>
</li>
</ul>



#### Examples


```cpp
DWORD    dwProvType;
HRESULT  hr;

// Get the ProviderType value.
// pEnroll is previously instantiated ICEnroll interface pointer
hr = pEnroll->get_ProviderType(&dwProvType);
if (FAILED( hr ))
    printf("Failed get_ProviderType - %x\n", hr);
else
    printf("ProviderType: %d\n", dwProvType);

// Set the ProviderType value.
hr = pEnroll->put_ProviderType(PROV_MS_EXCHANGE);
if (FAILED(hr))
    printf("Failed put_ProviderType - %x\n", hr);
else
    printf("ProviderType set to %d\n", PROV_MS_EXCHANGE);
```
