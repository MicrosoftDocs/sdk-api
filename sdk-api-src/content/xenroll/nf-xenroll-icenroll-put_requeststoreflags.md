---
UID: NF:xenroll.ICEnroll.put_RequestStoreFlags
title: ICEnroll::put_RequestStoreFlags (xenroll.h)
description: Sets or retrieves the registry location used for the request store. (Put)
helpviewer_keywords: ["CEnroll object [Security]","RequestStoreFlags property","ICEnroll interface [Security]","RequestStoreFlags property","ICEnroll.RequestStoreFlags","ICEnroll.put_RequestStoreFlags","ICEnroll2 interface [Security]","RequestStoreFlags property","ICEnroll2.RequestStoreFlags","ICEnroll2::get_RequestStoreFlags","ICEnroll2::put_RequestStoreFlags","ICEnroll3 interface [Security]","RequestStoreFlags property","ICEnroll3.RequestStoreFlags","ICEnroll3::get_RequestStoreFlags","ICEnroll3::put_RequestStoreFlags","ICEnroll4 interface [Security]","RequestStoreFlags property","ICEnroll4.RequestStoreFlags","ICEnroll4::RequestStoreFlags","ICEnroll4::get_RequestStoreFlags","ICEnroll4::put_RequestStoreFlags","ICEnroll::get_RequestStoreFlags","ICEnroll::put_RequestStoreFlags","RequestStoreFlags property [Security]","RequestStoreFlags property [Security]","CEnroll object","RequestStoreFlags property [Security]","ICEnroll interface","RequestStoreFlags property [Security]","ICEnroll2 interface","RequestStoreFlags property [Security]","ICEnroll3 interface","RequestStoreFlags property [Security]","ICEnroll4 interface","put_RequestStoreFlags","security.icenroll4_requeststoreflags","xenroll/ICEnroll2::RequestStoreFlags","xenroll/ICEnroll2::get_RequestStoreFlags","xenroll/ICEnroll2::put_RequestStoreFlags","xenroll/ICEnroll3::RequestStoreFlags","xenroll/ICEnroll3::get_RequestStoreFlags","xenroll/ICEnroll3::put_RequestStoreFlags","xenroll/ICEnroll4::RequestStoreFlags","xenroll/ICEnroll4::get_RequestStoreFlags","xenroll/ICEnroll4::put_RequestStoreFlags","xenroll/ICEnroll::RequestStoreFlags","xenroll/ICEnroll::get_RequestStoreFlags","xenroll/ICEnroll::put_RequestStoreFlags"]
old-location: security\icenroll4_requeststoreflags.htm
tech.root: security
ms.assetid: 399870f0-69e1-4a21-a7fa-c3de9ee66876
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],RequestStoreFlags property, ICEnroll interface [Security],RequestStoreFlags property, ICEnroll.RequestStoreFlags, ICEnroll.put_RequestStoreFlags, ICEnroll2 interface [Security],RequestStoreFlags property, ICEnroll2.RequestStoreFlags, ICEnroll2::get_RequestStoreFlags, ICEnroll2::put_RequestStoreFlags, ICEnroll3 interface [Security],RequestStoreFlags property, ICEnroll3.RequestStoreFlags, ICEnroll3::get_RequestStoreFlags, ICEnroll3::put_RequestStoreFlags, ICEnroll4 interface [Security],RequestStoreFlags property, ICEnroll4.RequestStoreFlags, ICEnroll4::RequestStoreFlags, ICEnroll4::get_RequestStoreFlags, ICEnroll4::put_RequestStoreFlags, ICEnroll::get_RequestStoreFlags, ICEnroll::put_RequestStoreFlags, RequestStoreFlags property [Security], RequestStoreFlags property [Security],CEnroll object, RequestStoreFlags property [Security],ICEnroll interface, RequestStoreFlags property [Security],ICEnroll2 interface, RequestStoreFlags property [Security],ICEnroll3 interface, RequestStoreFlags property [Security],ICEnroll4 interface, put_RequestStoreFlags, security.icenroll4_requeststoreflags, xenroll/ICEnroll2::RequestStoreFlags, xenroll/ICEnroll2::get_RequestStoreFlags, xenroll/ICEnroll2::put_RequestStoreFlags, xenroll/ICEnroll3::RequestStoreFlags, xenroll/ICEnroll3::get_RequestStoreFlags, xenroll/ICEnroll3::put_RequestStoreFlags, xenroll/ICEnroll4::RequestStoreFlags, xenroll/ICEnroll4::get_RequestStoreFlags, xenroll/ICEnroll4::put_RequestStoreFlags, xenroll/ICEnroll::RequestStoreFlags, xenroll/ICEnroll::get_RequestStoreFlags, xenroll/ICEnroll::put_RequestStoreFlags
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
 - ICEnroll::put_RequestStoreFlags
 - xenroll/ICEnroll::put_RequestStoreFlags
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
 - ICEnroll4.RequestStoreFlags
 - ICEnroll4.get_RequestStoreFlags
 - ICEnroll4.put_RequestStoreFlags
 - ICEnroll3.RequestStoreFlags
 - ICEnroll3.get_RequestStoreFlags
 - ICEnroll3.put_RequestStoreFlags
 - ICEnroll2.RequestStoreFlags
 - ICEnroll2.get_RequestStoreFlags
 - ICEnroll2.put_RequestStoreFlags
 - ICEnroll.RequestStoreFlags
 - ICEnroll.get_RequestStoreFlags
 - ICEnroll.put_RequestStoreFlags
 - CEnroll.RequestStoreFlags
---

# ICEnroll::put_RequestStoreFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreFlags</b> property sets or retrieves the registry location used for the request store.

 The default value for this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>RequestStoreFlags</b> property value is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> CryptoAPI function  by using its <i>dwFlags</i> parameter.

Typically, modification of the <b>RequestStoreFlags</b> property is  performed only in advanced applications.


The <b>RequestStoreFlags</b> property should be set before using the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
</ul>



#### Examples


```cpp
DWORD    dwFlags;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// retrieve the flag value
hr = pEnroll->get_RequestStoreFlags( &dwFlags );
if ( FAILED ( hr ) )
    printf("Failed retrieving RequestStoreFlags - %x\n", hr );
else
    printf("RequestStoreFlags is %x\n", dwFlags );

// set the flag
hr = pEnroll->put_RequestStoreFlags
   ( CERT_SYSTEM_STORE_LOCAL_MACHINE );
if ( FAILED ( hr ) )
    printf("Failed updating RequestStoreFlags - %x\n", hr );
else
    printf("Updated RequestStoreFlags\n");
```
