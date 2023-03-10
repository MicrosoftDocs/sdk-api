---
UID: NF:xenroll.ICEnroll.put_RootStoreType
title: ICEnroll::put_RootStoreType (xenroll.h)
description: Sets or retrieves the type of store to use for the store specified by the RootStoreName property. (Put)
helpviewer_keywords: ["CEnroll object [Security]","RootStoreType property","ICEnroll interface [Security]","RootStoreType property","ICEnroll.RootStoreType","ICEnroll.put_RootStoreType","ICEnroll2 interface [Security]","RootStoreType property","ICEnroll2.RootStoreType","ICEnroll2::get_RootStoreType","ICEnroll2::put_RootStoreType","ICEnroll3 interface [Security]","RootStoreType property","ICEnroll3.RootStoreType","ICEnroll3::get_RootStoreType","ICEnroll3::put_RootStoreType","ICEnroll4 interface [Security]","RootStoreType property","ICEnroll4.RootStoreType","ICEnroll4::RootStoreType","ICEnroll4::get_RootStoreType","ICEnroll4::put_RootStoreType","ICEnroll::get_RootStoreType","ICEnroll::put_RootStoreType","RootStoreType property [Security]","RootStoreType property [Security]","CEnroll object","RootStoreType property [Security]","ICEnroll interface","RootStoreType property [Security]","ICEnroll2 interface","RootStoreType property [Security]","ICEnroll3 interface","RootStoreType property [Security]","ICEnroll4 interface","put_RootStoreType","security.icenroll4_rootstoretype","sz_CERT_STORE_PROV_SYSTEM","sz_CERT_STORE_PROV_SYSTEM_W","xenroll/ICEnroll2::RootStoreType","xenroll/ICEnroll2::get_RootStoreType","xenroll/ICEnroll2::put_RootStoreType","xenroll/ICEnroll3::RootStoreType","xenroll/ICEnroll3::get_RootStoreType","xenroll/ICEnroll3::put_RootStoreType","xenroll/ICEnroll4::RootStoreType","xenroll/ICEnroll4::get_RootStoreType","xenroll/ICEnroll4::put_RootStoreType","xenroll/ICEnroll::RootStoreType","xenroll/ICEnroll::get_RootStoreType","xenroll/ICEnroll::put_RootStoreType"]
old-location: security\icenroll4_rootstoretype.htm
tech.root: security
ms.assetid: 452f89ad-e512-4ac7-816a-c3f97e25350a
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],RootStoreType property, ICEnroll interface [Security],RootStoreType property, ICEnroll.RootStoreType, ICEnroll.put_RootStoreType, ICEnroll2 interface [Security],RootStoreType property, ICEnroll2.RootStoreType, ICEnroll2::get_RootStoreType, ICEnroll2::put_RootStoreType, ICEnroll3 interface [Security],RootStoreType property, ICEnroll3.RootStoreType, ICEnroll3::get_RootStoreType, ICEnroll3::put_RootStoreType, ICEnroll4 interface [Security],RootStoreType property, ICEnroll4.RootStoreType, ICEnroll4::RootStoreType, ICEnroll4::get_RootStoreType, ICEnroll4::put_RootStoreType, ICEnroll::get_RootStoreType, ICEnroll::put_RootStoreType, RootStoreType property [Security], RootStoreType property [Security],CEnroll object, RootStoreType property [Security],ICEnroll interface, RootStoreType property [Security],ICEnroll2 interface, RootStoreType property [Security],ICEnroll3 interface, RootStoreType property [Security],ICEnroll4 interface, put_RootStoreType, security.icenroll4_rootstoretype, sz_CERT_STORE_PROV_SYSTEM, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/ICEnroll2::RootStoreType, xenroll/ICEnroll2::get_RootStoreType, xenroll/ICEnroll2::put_RootStoreType, xenroll/ICEnroll3::RootStoreType, xenroll/ICEnroll3::get_RootStoreType, xenroll/ICEnroll3::put_RootStoreType, xenroll/ICEnroll4::RootStoreType, xenroll/ICEnroll4::get_RootStoreType, xenroll/ICEnroll4::put_RootStoreType, xenroll/ICEnroll::RootStoreType, xenroll/ICEnroll::get_RootStoreType, xenroll/ICEnroll::put_RootStoreType
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
 - ICEnroll::put_RootStoreType
 - xenroll/ICEnroll::put_RootStoreType
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
 - ICEnroll4.RootStoreType
 - ICEnroll4.get_RootStoreType
 - ICEnroll4.put_RootStoreType
 - ICEnroll3.RootStoreType
 - ICEnroll3.get_RootStoreType
 - ICEnroll3.put_RootStoreType
 - ICEnroll2.RootStoreType
 - ICEnroll2.get_RootStoreType
 - ICEnroll2.put_RootStoreType
 - ICEnroll.RootStoreType
 - ICEnroll.get_RootStoreType
 - ICEnroll.put_RootStoreType
 - CEnroll.RootStoreType
---

# ICEnroll::put_RootStoreType


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreType</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a> property. This store type is passed directly on to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> function.

The default value for this property is sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

<b>RootStoreType</b> affects the behavior of the following methods:

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
hr = pEnroll->get_RootStoreType( &bstrStoreType );
if ( FAILED ( hr ) )
    printf("Failed getting RootStoreType - %x\n", hr );
else
    printf( "RootStoreType: %ws\n", bstrStoreType );
// free BSTR when done
if ( NULL != bstrStoreType )
    SysFreeString( bstrStoreType );

// set the storetype
// bstrNewType is a BSTR that is previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
if ( FAILED ( hr ) )
    printf("Failed setting RootStoreType - %x\n", hr );
else
    printf( "RootStoreType was set to %ws\n", bstrNewType );
```
