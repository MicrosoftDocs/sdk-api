---
UID: NF:xenroll.ICEnroll.put_HashAlgorithm
title: ICEnroll::put_HashAlgorithm (xenroll.h)
description: Sets or retrieves only the signature hashing algorithm used to sign the PKCS (ICEnroll.put_HashAlgorithm)
helpviewer_keywords: ["CEnroll object [Security]","HashAlgorithm property","HashAlgorithm property [Security]","HashAlgorithm property [Security]","CEnroll object","HashAlgorithm property [Security]","ICEnroll interface","HashAlgorithm property [Security]","ICEnroll2 interface","HashAlgorithm property [Security]","ICEnroll3 interface","HashAlgorithm property [Security]","ICEnroll4 interface","ICEnroll interface [Security]","HashAlgorithm property","ICEnroll.HashAlgorithm","ICEnroll.put_HashAlgorithm","ICEnroll2 interface [Security]","HashAlgorithm property","ICEnroll2.HashAlgorithm","ICEnroll2::get_HashAlgorithm","ICEnroll2::put_HashAlgorithm","ICEnroll3 interface [Security]","HashAlgorithm property","ICEnroll3.HashAlgorithm","ICEnroll3::get_HashAlgorithm","ICEnroll3::put_HashAlgorithm","ICEnroll4 interface [Security]","HashAlgorithm property","ICEnroll4.HashAlgorithm","ICEnroll4::HashAlgorithm","ICEnroll4::get_HashAlgorithm","ICEnroll4::put_HashAlgorithm","ICEnroll::get_HashAlgorithm","ICEnroll::put_HashAlgorithm","put_HashAlgorithm","security.icenroll4_hashalgorithm","xenroll/ICEnroll2::HashAlgorithm","xenroll/ICEnroll2::get_HashAlgorithm","xenroll/ICEnroll2::put_HashAlgorithm","xenroll/ICEnroll3::HashAlgorithm","xenroll/ICEnroll3::get_HashAlgorithm","xenroll/ICEnroll3::put_HashAlgorithm","xenroll/ICEnroll4::HashAlgorithm","xenroll/ICEnroll4::get_HashAlgorithm","xenroll/ICEnroll4::put_HashAlgorithm","xenroll/ICEnroll::HashAlgorithm","xenroll/ICEnroll::get_HashAlgorithm","xenroll/ICEnroll::put_HashAlgorithm"]
old-location: security\icenroll4_hashalgorithm.htm
tech.root: security
ms.assetid: 48f8a47b-0ab4-4150-b8cf-37e57fb04d3e
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],HashAlgorithm property, HashAlgorithm property [Security], HashAlgorithm property [Security],CEnroll object, HashAlgorithm property [Security],ICEnroll interface, HashAlgorithm property [Security],ICEnroll2 interface, HashAlgorithm property [Security],ICEnroll3 interface, HashAlgorithm property [Security],ICEnroll4 interface, ICEnroll interface [Security],HashAlgorithm property, ICEnroll.HashAlgorithm, ICEnroll.put_HashAlgorithm, ICEnroll2 interface [Security],HashAlgorithm property, ICEnroll2.HashAlgorithm, ICEnroll2::get_HashAlgorithm, ICEnroll2::put_HashAlgorithm, ICEnroll3 interface [Security],HashAlgorithm property, ICEnroll3.HashAlgorithm, ICEnroll3::get_HashAlgorithm, ICEnroll3::put_HashAlgorithm, ICEnroll4 interface [Security],HashAlgorithm property, ICEnroll4.HashAlgorithm, ICEnroll4::HashAlgorithm, ICEnroll4::get_HashAlgorithm, ICEnroll4::put_HashAlgorithm, ICEnroll::get_HashAlgorithm, ICEnroll::put_HashAlgorithm, put_HashAlgorithm, security.icenroll4_hashalgorithm, xenroll/ICEnroll2::HashAlgorithm, xenroll/ICEnroll2::get_HashAlgorithm, xenroll/ICEnroll2::put_HashAlgorithm, xenroll/ICEnroll3::HashAlgorithm, xenroll/ICEnroll3::get_HashAlgorithm, xenroll/ICEnroll3::put_HashAlgorithm, xenroll/ICEnroll4::HashAlgorithm, xenroll/ICEnroll4::get_HashAlgorithm, xenroll/ICEnroll4::put_HashAlgorithm, xenroll/ICEnroll::HashAlgorithm, xenroll/ICEnroll::get_HashAlgorithm, xenroll/ICEnroll::put_HashAlgorithm
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
 - ICEnroll::put_HashAlgorithm
 - xenroll/ICEnroll::put_HashAlgorithm
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
 - ICEnroll4.HashAlgorithm
 - ICEnroll4.get_HashAlgorithm
 - ICEnroll4.put_HashAlgorithm
 - ICEnroll3.HashAlgorithm
 - ICEnroll3.get_HashAlgorithm
 - ICEnroll3.put_HashAlgorithm
 - ICEnroll2.HashAlgorithm
 - ICEnroll2.get_HashAlgorithm
 - ICEnroll2.put_HashAlgorithm
 - ICEnroll.HashAlgorithm
 - ICEnroll.get_HashAlgorithm
 - ICEnroll.put_HashAlgorithm
 - CEnroll.HashAlgorithm
---

# ICEnroll::put_HashAlgorithm


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgorithm</b> property sets or retrieves only   the signature <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> used to sign the PKCS #10 certification request.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

This  signature <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> is not to be confused with the <i>hashing algorithm</i> used to sign the certificate. The enrollment control currently supports any <a href="/windows/desktop/SecGloss/o-gly">OID</a> for <i>hashing algorithms</i>, plus the following display name values: SHA1 (the default), MD2, and MD5. When retrieving this property, the retrieved value is in OID format (that is, SHA1 appears as 1.3.14.3.2.29). When setting this property, the corresponding OID format can be used as an alternative to the text shown for the defined friendly values.

The Certificate Enrollment Control considers the value of the <b>HashAlgorithm</b> property  as a hint to the <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> to use for signing the PKCS #10 certification request. If the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) supports the algorithm specified in the <b>HashAlgorithm</b> property, the algorithm will be used. Otherwise, the Certificate Enrollment Control will try to use SHA1. If SHA1 is not supported by the CSP, then MD5 will be tried. If neither SHA1 nor MD5 is supported, the Certificate Enrollment Control will try to use the first <i>hashing algorithm</i> returned from the CSP.


The <b>HashAlgorithm</b>  property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
</ul>


If both the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">HashAlgID</a> and <b>HashAlgorithm</b> properties are set, whichever is last updated will specify which <a href="/windows/desktop/SecGloss/h-gly">hashing algorithm</a> will be used to sign the PKCS #10 certification request.


#### Examples


```cpp
BSTR     bstrHashAlg = NULL;
HRESULT  hr;

// get the hash algorithm
hr = pEnroll->get_HashAlgorithm( &bstrHashAlg );
if ( FAILED ( hr ) )
    printf("Failed get_HashAlgorithm - %x\n", hr );
else
    printf( "HashAlgorithm: %ws\n", bstrHashAlg );
// free BSTR
if ( NULL != bstrHashAlg )
    SysFreeString( bstrHashAlg);

BSTR    bstrMyHashAlg = SysAllocString(TEXT("MD5"));
// alternatively, ... = SysAllocString(TEXT("1.2.840.113549.1.1.4"));

// set the hash algorithm
hr = pEnroll->put_HashAlgorithm( bstrMyHashAlg );
if ( FAILED ( hr ) )
    printf("Failed put_HashAlgorithm - %x\n", hr );
else
    printf( "HashAlgorithm was set to %ws\n", bstrMyHashAlg );
// free BSTR
if ( NULL != bstrMyHashAlg )
    SysFreeString( bstrMyHashAlg);
```
