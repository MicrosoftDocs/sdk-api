---
UID: NF:xenroll.ICEnroll.get_ProviderFlags
title: ICEnroll::get_ProviderFlags (xenroll.h)
description: Sets or retrieves the provider type. (Get)
helpviewer_keywords: ["CEnroll object [Security]","ProviderFlags property","ICEnroll interface [Security]","ProviderFlags property","ICEnroll.ProviderFlags","ICEnroll.get_ProviderFlags","ICEnroll2 interface [Security]","ProviderFlags property","ICEnroll2.ProviderFlags","ICEnroll2::get_ProviderFlags","ICEnroll2::put_ProviderFlags","ICEnroll3 interface [Security]","ProviderFlags property","ICEnroll3.ProviderFlags","ICEnroll3::get_ProviderFlags","ICEnroll3::put_ProviderFlags","ICEnroll4 interface [Security]","ProviderFlags property","ICEnroll4.ProviderFlags","ICEnroll4::ProviderFlags","ICEnroll4::get_ProviderFlags","ICEnroll4::put_ProviderFlags","ICEnroll::get_ProviderFlags","ICEnroll::put_ProviderFlags","ProviderFlags property [Security]","ProviderFlags property [Security]","CEnroll object","ProviderFlags property [Security]","ICEnroll interface","ProviderFlags property [Security]","ICEnroll2 interface","ProviderFlags property [Security]","ICEnroll3 interface","ProviderFlags property [Security]","ICEnroll4 interface","get_ProviderFlags","security.icenroll4_providerflags","xenroll/ICEnroll2::ProviderFlags","xenroll/ICEnroll2::get_ProviderFlags","xenroll/ICEnroll2::put_ProviderFlags","xenroll/ICEnroll3::ProviderFlags","xenroll/ICEnroll3::get_ProviderFlags","xenroll/ICEnroll3::put_ProviderFlags","xenroll/ICEnroll4::ProviderFlags","xenroll/ICEnroll4::get_ProviderFlags","xenroll/ICEnroll4::put_ProviderFlags","xenroll/ICEnroll::ProviderFlags","xenroll/ICEnroll::get_ProviderFlags","xenroll/ICEnroll::put_ProviderFlags"]
old-location: security\icenroll4_providerflags.htm
tech.root: security
ms.assetid: ddf92921-368f-4769-b2c1-b9d6a94b0fcb
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],ProviderFlags property, ICEnroll interface [Security],ProviderFlags property, ICEnroll.ProviderFlags, ICEnroll.get_ProviderFlags, ICEnroll2 interface [Security],ProviderFlags property, ICEnroll2.ProviderFlags, ICEnroll2::get_ProviderFlags, ICEnroll2::put_ProviderFlags, ICEnroll3 interface [Security],ProviderFlags property, ICEnroll3.ProviderFlags, ICEnroll3::get_ProviderFlags, ICEnroll3::put_ProviderFlags, ICEnroll4 interface [Security],ProviderFlags property, ICEnroll4.ProviderFlags, ICEnroll4::ProviderFlags, ICEnroll4::get_ProviderFlags, ICEnroll4::put_ProviderFlags, ICEnroll::get_ProviderFlags, ICEnroll::put_ProviderFlags, ProviderFlags property [Security], ProviderFlags property [Security],CEnroll object, ProviderFlags property [Security],ICEnroll interface, ProviderFlags property [Security],ICEnroll2 interface, ProviderFlags property [Security],ICEnroll3 interface, ProviderFlags property [Security],ICEnroll4 interface, get_ProviderFlags, security.icenroll4_providerflags, xenroll/ICEnroll2::ProviderFlags, xenroll/ICEnroll2::get_ProviderFlags, xenroll/ICEnroll2::put_ProviderFlags, xenroll/ICEnroll3::ProviderFlags, xenroll/ICEnroll3::get_ProviderFlags, xenroll/ICEnroll3::put_ProviderFlags, xenroll/ICEnroll4::ProviderFlags, xenroll/ICEnroll4::get_ProviderFlags, xenroll/ICEnroll4::put_ProviderFlags, xenroll/ICEnroll::ProviderFlags, xenroll/ICEnroll::get_ProviderFlags, xenroll/ICEnroll::put_ProviderFlags
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
 - ICEnroll::get_ProviderFlags
 - xenroll/ICEnroll::get_ProviderFlags
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
 - ICEnroll4.ProviderFlags
 - ICEnroll4.get_ProviderFlags
 - ICEnroll4.put_ProviderFlags
 - ICEnroll3.ProviderFlags
 - ICEnroll3.get_ProviderFlags
 - ICEnroll3.put_ProviderFlags
 - ICEnroll2.ProviderFlags
 - ICEnroll2.get_ProviderFlags
 - ICEnroll2.put_ProviderFlags
 - ICEnroll.ProviderFlags
 - ICEnroll.get_ProviderFlags
 - ICEnroll.put_ProviderFlags
 - CEnroll.ProviderFlags
---

# ICEnroll::get_ProviderFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderFlags</b> property sets or retrieves the provider type.

The <b>ProviderFlags</b> property is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use.

The default value for this property is zero. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

For  more information about   valid <b>ProviderFlags</b> values for the Microsoft Base Cryptographic Provider, see the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI function.

For information about  other CSPs, see the documentation provided with the CSP.

The <b>ProviderFlags</b> property value is passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  by using  its <i>dwFlags</i> parameter.


The <b>ProviderFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
</ul>



#### Examples


```cpp
DWORD    dwProvFlags;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer
// get the ProviderFlags value
hr = pEnroll->get_ProviderFlags( &dwProvFlags );
if (FAILED( hr ))
    printf("Failed get_ProviderFlags - %x\n", hr );
else
    printf( "ProviderFlags: %d\n", dwProvFlags );

// Set the ProviderFlags value.
hr = pEnroll->put_ProviderFlags(CRYPT_MACHINE_KEYSET);
if (FAILED( hr ))
    printf("Failed put_ProviderFlags - %x\n", hr );
else
    printf( "ProviderFlags set to %d\n", CRYPT_MACHINE_KEYSET  );
```
