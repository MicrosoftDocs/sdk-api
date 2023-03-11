---
UID: NF:xenroll.ICEnroll.get_RequestStoreName
title: ICEnroll::get_RequestStoreName (xenroll.h)
description: Sets or retrievesICEnroll the name of the store that contains the dummy certificate. (Get)
helpviewer_keywords: ["CEnroll object [Security]","RequestStoreName property","ICEnroll interface [Security]","RequestStoreName property","ICEnroll.RequestStoreName","ICEnroll.get_RequestStoreName","ICEnroll2 interface [Security]","RequestStoreName property","ICEnroll2.RequestStoreName","ICEnroll2::get_RequestStoreName","ICEnroll2::put_RequestStoreName","ICEnroll3 interface [Security]","RequestStoreName property","ICEnroll3.RequestStoreName","ICEnroll3::get_RequestStoreName","ICEnroll3::put_RequestStoreName","ICEnroll4 interface [Security]","RequestStoreName property","ICEnroll4.RequestStoreName","ICEnroll4::RequestStoreName","ICEnroll4::get_RequestStoreName","ICEnroll4::put_RequestStoreName","ICEnroll::get_RequestStoreName","ICEnroll::put_RequestStoreName","RequestStoreName property [Security]","RequestStoreName property [Security]","CEnroll object","RequestStoreName property [Security]","ICEnroll interface","RequestStoreName property [Security]","ICEnroll2 interface","RequestStoreName property [Security]","ICEnroll3 interface","RequestStoreName property [Security]","ICEnroll4 interface","get_RequestStoreName","security.icenroll4_requeststorename","xenroll/ICEnroll2::RequestStoreName","xenroll/ICEnroll2::get_RequestStoreName","xenroll/ICEnroll2::put_RequestStoreName","xenroll/ICEnroll3::RequestStoreName","xenroll/ICEnroll3::get_RequestStoreName","xenroll/ICEnroll3::put_RequestStoreName","xenroll/ICEnroll4::RequestStoreName","xenroll/ICEnroll4::get_RequestStoreName","xenroll/ICEnroll4::put_RequestStoreName","xenroll/ICEnroll::RequestStoreName","xenroll/ICEnroll::get_RequestStoreName","xenroll/ICEnroll::put_RequestStoreName"]
old-location: security\icenroll4_requeststorename.htm
tech.root: security
ms.assetid: c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],RequestStoreName property, ICEnroll interface [Security],RequestStoreName property, ICEnroll.RequestStoreName, ICEnroll.get_RequestStoreName, ICEnroll2 interface [Security],RequestStoreName property, ICEnroll2.RequestStoreName, ICEnroll2::get_RequestStoreName, ICEnroll2::put_RequestStoreName, ICEnroll3 interface [Security],RequestStoreName property, ICEnroll3.RequestStoreName, ICEnroll3::get_RequestStoreName, ICEnroll3::put_RequestStoreName, ICEnroll4 interface [Security],RequestStoreName property, ICEnroll4.RequestStoreName, ICEnroll4::RequestStoreName, ICEnroll4::get_RequestStoreName, ICEnroll4::put_RequestStoreName, ICEnroll::get_RequestStoreName, ICEnroll::put_RequestStoreName, RequestStoreName property [Security], RequestStoreName property [Security],CEnroll object, RequestStoreName property [Security],ICEnroll interface, RequestStoreName property [Security],ICEnroll2 interface, RequestStoreName property [Security],ICEnroll3 interface, RequestStoreName property [Security],ICEnroll4 interface, get_RequestStoreName, security.icenroll4_requeststorename, xenroll/ICEnroll2::RequestStoreName, xenroll/ICEnroll2::get_RequestStoreName, xenroll/ICEnroll2::put_RequestStoreName, xenroll/ICEnroll3::RequestStoreName, xenroll/ICEnroll3::get_RequestStoreName, xenroll/ICEnroll3::put_RequestStoreName, xenroll/ICEnroll4::RequestStoreName, xenroll/ICEnroll4::get_RequestStoreName, xenroll/ICEnroll4::put_RequestStoreName, xenroll/ICEnroll::RequestStoreName, xenroll/ICEnroll::get_RequestStoreName, xenroll/ICEnroll::put_RequestStoreName
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
 - ICEnroll::get_RequestStoreName
 - xenroll/ICEnroll::get_RequestStoreName
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
 - ICEnroll4.RequestStoreName
 - ICEnroll4.get_RequestStoreName
 - ICEnroll4.put_RequestStoreName
 - ICEnroll3.RequestStoreName
 - ICEnroll3.get_RequestStoreName
 - ICEnroll3.put_RequestStoreName
 - ICEnroll2.RequestStoreName
 - ICEnroll2.get_RequestStoreName
 - ICEnroll2.put_RequestStoreName
 - ICEnroll.RequestStoreName
 - ICEnroll.get_RequestStoreName
 - ICEnroll.put_RequestStoreName
 - CEnroll.RequestStoreName
---

# ICEnroll::get_RequestStoreName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreName</b> property sets or retrieves<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> processes the request and responds with a PKCS #7.

The default value for this property is  "REQUEST". If the default is not to be used, this property must be set to the store to be used before calls to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a> or <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a> and again before calls to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a> or <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

Typically, modification of the <b>RequestStoreName</b> property is  performed only in advanced applications. Changing this value is not recommended for most applications.


The <b>RequestStoreName</b> property affects the behavior of the following methods:

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


The ability to set this property is disabled when  the Certificate Enrollment Control is executed as a scripted control.


#### Examples


```cpp
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storename
hr = pEnroll->get_RequestStoreName( &bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting RequestStoreName - %x\n", hr );
else
    printf( "RequestStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName is a BSTR that is previously set to a valid store name
hr = pEnroll->put_RequestStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting RequestStoreName - %x\n", hr );
else
    printf( "RequestStoreName was set to : %ws\n", bstrNewName );
```
