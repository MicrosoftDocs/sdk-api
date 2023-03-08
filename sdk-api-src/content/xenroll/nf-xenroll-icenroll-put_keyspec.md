---
UID: NF:xenroll.ICEnroll.put_KeySpec
title: ICEnroll::put_KeySpec (xenroll.h)
description: The KeySpec property of ICEnroll4 sets or retrieves the type of key generated. (Put)
helpviewer_keywords: ["CEnroll object [Security]","KeySpec property","ICEnroll interface [Security]","KeySpec property","ICEnroll.KeySpec","ICEnroll.put_KeySpec","ICEnroll2 interface [Security]","KeySpec property","ICEnroll2.KeySpec","ICEnroll2::get_KeySpec","ICEnroll2::put_KeySpec","ICEnroll3 interface [Security]","KeySpec property","ICEnroll3.KeySpec","ICEnroll3::get_KeySpec","ICEnroll3::put_KeySpec","ICEnroll4 interface [Security]","KeySpec property","ICEnroll4.KeySpec","ICEnroll4::KeySpec","ICEnroll4::get_KeySpec","ICEnroll4::put_KeySpec","ICEnroll::get_KeySpec","ICEnroll::put_KeySpec","KeySpec property [Security]","KeySpec property [Security]","CEnroll object","KeySpec property [Security]","ICEnroll interface","KeySpec property [Security]","ICEnroll2 interface","KeySpec property [Security]","ICEnroll3 interface","KeySpec property [Security]","ICEnroll4 interface","put_KeySpec","security.icenroll4_keyspec","xenroll/ICEnroll2::KeySpec","xenroll/ICEnroll2::get_KeySpec","xenroll/ICEnroll2::put_KeySpec","xenroll/ICEnroll3::KeySpec","xenroll/ICEnroll3::get_KeySpec","xenroll/ICEnroll3::put_KeySpec","xenroll/ICEnroll4::KeySpec","xenroll/ICEnroll4::get_KeySpec","xenroll/ICEnroll4::put_KeySpec","xenroll/ICEnroll::KeySpec","xenroll/ICEnroll::get_KeySpec","xenroll/ICEnroll::put_KeySpec"]
old-location: security\icenroll4_keyspec.htm
tech.root: security
ms.assetid: 30cc7c86-29ce-42e9-b9dc-d29f5b5450a5
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],KeySpec property, ICEnroll interface [Security],KeySpec property, ICEnroll.KeySpec, ICEnroll.put_KeySpec, ICEnroll2 interface [Security],KeySpec property, ICEnroll2.KeySpec, ICEnroll2::get_KeySpec, ICEnroll2::put_KeySpec, ICEnroll3 interface [Security],KeySpec property, ICEnroll3.KeySpec, ICEnroll3::get_KeySpec, ICEnroll3::put_KeySpec, ICEnroll4 interface [Security],KeySpec property, ICEnroll4.KeySpec, ICEnroll4::KeySpec, ICEnroll4::get_KeySpec, ICEnroll4::put_KeySpec, ICEnroll::get_KeySpec, ICEnroll::put_KeySpec, KeySpec property [Security], KeySpec property [Security],CEnroll object, KeySpec property [Security],ICEnroll interface, KeySpec property [Security],ICEnroll2 interface, KeySpec property [Security],ICEnroll3 interface, KeySpec property [Security],ICEnroll4 interface, put_KeySpec, security.icenroll4_keyspec, xenroll/ICEnroll2::KeySpec, xenroll/ICEnroll2::get_KeySpec, xenroll/ICEnroll2::put_KeySpec, xenroll/ICEnroll3::KeySpec, xenroll/ICEnroll3::get_KeySpec, xenroll/ICEnroll3::put_KeySpec, xenroll/ICEnroll4::KeySpec, xenroll/ICEnroll4::get_KeySpec, xenroll/ICEnroll4::put_KeySpec, xenroll/ICEnroll::KeySpec, xenroll/ICEnroll::get_KeySpec, xenroll/ICEnroll::put_KeySpec
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
 - ICEnroll::put_KeySpec
 - xenroll/ICEnroll::put_KeySpec
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
 - ICEnroll4.KeySpec
 - ICEnroll4.get_KeySpec
 - ICEnroll4.put_KeySpec
 - ICEnroll3.KeySpec
 - ICEnroll3.get_KeySpec
 - ICEnroll3.put_KeySpec
 - ICEnroll2.KeySpec
 - ICEnroll2.get_KeySpec
 - ICEnroll2.put_KeySpec
 - ICEnroll.KeySpec
 - ICEnroll.get_KeySpec
 - ICEnroll.put_KeySpec
 - CEnroll.KeySpec
---

# ICEnroll::put_KeySpec


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>KeySpec</b> property sets or retrieves the  type of key generated.

 Valid values are determined by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) in use. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has a value of AT_KEYEXCHANGE for <a href="/windows/desktop/SecGloss/e-gly">exchange keys</a>, or AT_SIGNATURE for signature keys. The default is AT_SIGNATURE.

For information about the other Microsoft CSPs, see 
<a href="/windows/desktop/SecCrypto/cryptographic-service-providers">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about other CSPs, see the documentation provided with the CSP.


The <b>KeySpec</b> property affects the behavior of the following methods:

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
DWORD    dwKeySpec;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the KeySpec value
hr = pEnroll->get_KeySpec( &dwKeySpec );
if (FAILED( hr ))
    printf("Failed get_KeySpec - %x\n", hr );
else
    printf( "KeySpec: %d\n", dwKeySpec );

// set the KeySpec value
hr = pEnroll->put_KeySpec( AT_KEYEXCHANGE );
if (FAILED( hr ))
    printf("Failed put_KeySpec - %x\n", hr );
else
    printf( "KeySpec set to %d\n", AT_KEYEXCHANGE );
```
