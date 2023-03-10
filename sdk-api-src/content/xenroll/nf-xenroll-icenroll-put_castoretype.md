---
UID: NF:xenroll.ICEnroll.put_CAStoreType
title: ICEnroll::put_CAStoreType (xenroll.h)
description: Sets or retrieves the type of store to use for the store specified by the CAStoreName property. (Put)
helpviewer_keywords: ["CAStoreType property [Security]","CAStoreType property [Security]","CEnroll object","CAStoreType property [Security]","ICEnroll interface","CAStoreType property [Security]","ICEnroll2 interface","CAStoreType property [Security]","ICEnroll3 interface","CAStoreType property [Security]","ICEnroll4 interface","CEnroll object [Security]","CAStoreType property","ICEnroll interface [Security]","CAStoreType property","ICEnroll.CAStoreType","ICEnroll.put_CAStoreType","ICEnroll2 interface [Security]","CAStoreType property","ICEnroll2.CAStoreType","ICEnroll2::get_CAStoreType","ICEnroll2::put_CAStoreType","ICEnroll3 interface [Security]","CAStoreType property","ICEnroll3.CAStoreType","ICEnroll3::get_CAStoreType","ICEnroll3::put_CAStoreType","ICEnroll4 interface [Security]","CAStoreType property","ICEnroll4.CAStoreType","ICEnroll4::CAStoreType","ICEnroll4::get_CAStoreType","ICEnroll4::put_CAStoreType","ICEnroll::get_CAStoreType","ICEnroll::put_CAStoreType","put_CAStoreType","security.icenroll4_castoretype","sz_CERT_STORE_PROV_SYSTEM","sz_CERT_STORE_PROV_SYSTEM_W","xenroll/ICEnroll2::CAStoreType","xenroll/ICEnroll2::get_CAStoreType","xenroll/ICEnroll2::put_CAStoreType","xenroll/ICEnroll3::CAStoreType","xenroll/ICEnroll3::get_CAStoreType","xenroll/ICEnroll3::put_CAStoreType","xenroll/ICEnroll4::CAStoreType","xenroll/ICEnroll4::get_CAStoreType","xenroll/ICEnroll4::put_CAStoreType","xenroll/ICEnroll::CAStoreType","xenroll/ICEnroll::get_CAStoreType","xenroll/ICEnroll::put_CAStoreType"]
old-location: security\icenroll4_castoretype.htm
tech.root: security
ms.assetid: 8b0b113d-4046-4b2b-8f3b-ad08bfe3d0ac
ms.date: 12/05/2018
ms.keywords: CAStoreType property [Security], CAStoreType property [Security],CEnroll object, CAStoreType property [Security],ICEnroll interface, CAStoreType property [Security],ICEnroll2 interface, CAStoreType property [Security],ICEnroll3 interface, CAStoreType property [Security],ICEnroll4 interface, CEnroll object [Security],CAStoreType property, ICEnroll interface [Security],CAStoreType property, ICEnroll.CAStoreType, ICEnroll.put_CAStoreType, ICEnroll2 interface [Security],CAStoreType property, ICEnroll2.CAStoreType, ICEnroll2::get_CAStoreType, ICEnroll2::put_CAStoreType, ICEnroll3 interface [Security],CAStoreType property, ICEnroll3.CAStoreType, ICEnroll3::get_CAStoreType, ICEnroll3::put_CAStoreType, ICEnroll4 interface [Security],CAStoreType property, ICEnroll4.CAStoreType, ICEnroll4::CAStoreType, ICEnroll4::get_CAStoreType, ICEnroll4::put_CAStoreType, ICEnroll::get_CAStoreType, ICEnroll::put_CAStoreType, put_CAStoreType, security.icenroll4_castoretype, sz_CERT_STORE_PROV_SYSTEM, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/ICEnroll2::CAStoreType, xenroll/ICEnroll2::get_CAStoreType, xenroll/ICEnroll2::put_CAStoreType, xenroll/ICEnroll3::CAStoreType, xenroll/ICEnroll3::get_CAStoreType, xenroll/ICEnroll3::put_CAStoreType, xenroll/ICEnroll4::CAStoreType, xenroll/ICEnroll4::get_CAStoreType, xenroll/ICEnroll4::put_CAStoreType, xenroll/ICEnroll::CAStoreType, xenroll/ICEnroll::get_CAStoreType, xenroll/ICEnroll::put_CAStoreType
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
 - ICEnroll::put_CAStoreType
 - xenroll/ICEnroll::put_CAStoreType
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
 - ICEnroll4.CAStoreType
 - ICEnroll4.get_CAStoreType
 - ICEnroll4.put_CAStoreType
 - ICEnroll3.CAStoreType
 - ICEnroll3.get_CAStoreType
 - ICEnroll3.put_CAStoreType
 - ICEnroll2.CAStoreType
 - ICEnroll2.get_CAStoreType
 - ICEnroll2.put_CAStoreType
 - ICEnroll.CAStoreType
 - ICEnroll.get_CAStoreType
 - ICEnroll.put_CAStoreType
 - CEnroll.CAStoreType
---

# ICEnroll::put_CAStoreType


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreType</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a> property. This store type is passed directly on to the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

The default value for this property is  sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>CAStoreType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
</li>
</ul>


The ability to set this property is disabled when  the Certificate Enrollment Control is executed as a scripted control.


#### Examples


```cpp
BSTR     bstrStoreType = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storetype
hr = pEnroll->get_CAStoreType( &bstrStoreType );
if ( FAILED ( hr ) )
    printf("Failed getting CAStoreType - %x\n", hr );
else
    printf( "CAStoreType: %ws\n", bstrStoreType );
// free BSTR when done
if ( NULL != bstrStoreType )
    SysFreeString( bstrStoreType );

// set the storetype
// bstrNewType previously set to a valid store type
hr = pEnroll->put_CAStoreType( bstrNewType );
if ( FAILED ( hr ) )
    printf("Failed setting CAStoreType - %x\n", hr );
else
    printf( "CAStoreType was set to %ws\n", bstrNewType );
```
