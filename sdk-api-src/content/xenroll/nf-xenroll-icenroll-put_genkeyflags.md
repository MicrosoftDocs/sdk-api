---
UID: NF:xenroll.ICEnroll.put_GenKeyFlags
title: ICEnroll::put_GenKeyFlags (xenroll.h)
description: Sets or retrieves the values passed to the CryptGenKey function when the certificate request is generated. (Put)
helpviewer_keywords: ["CEnroll object [Security]","GenKeyFlags property","GenKeyFlags property [Security]","GenKeyFlags property [Security]","CEnroll object","GenKeyFlags property [Security]","ICEnroll interface","GenKeyFlags property [Security]","ICEnroll2 interface","GenKeyFlags property [Security]","ICEnroll3 interface","GenKeyFlags property [Security]","ICEnroll4 interface","ICEnroll interface [Security]","GenKeyFlags property","ICEnroll.GenKeyFlags","ICEnroll.put_GenKeyFlags","ICEnroll2 interface [Security]","GenKeyFlags property","ICEnroll2.GenKeyFlags","ICEnroll2::get_GenKeyFlags","ICEnroll2::put_GenKeyFlags","ICEnroll3 interface [Security]","GenKeyFlags property","ICEnroll3.GenKeyFlags","ICEnroll3::get_GenKeyFlags","ICEnroll3::put_GenKeyFlags","ICEnroll4 interface [Security]","GenKeyFlags property","ICEnroll4.GenKeyFlags","ICEnroll4::GenKeyFlags","ICEnroll4::get_GenKeyFlags","ICEnroll4::put_GenKeyFlags","ICEnroll::get_GenKeyFlags","ICEnroll::put_GenKeyFlags","put_GenKeyFlags","security.icenroll4_genkeyflags","xenroll/ICEnroll2::GenKeyFlags","xenroll/ICEnroll2::get_GenKeyFlags","xenroll/ICEnroll2::put_GenKeyFlags","xenroll/ICEnroll3::GenKeyFlags","xenroll/ICEnroll3::get_GenKeyFlags","xenroll/ICEnroll3::put_GenKeyFlags","xenroll/ICEnroll4::GenKeyFlags","xenroll/ICEnroll4::get_GenKeyFlags","xenroll/ICEnroll4::put_GenKeyFlags","xenroll/ICEnroll::GenKeyFlags","xenroll/ICEnroll::get_GenKeyFlags","xenroll/ICEnroll::put_GenKeyFlags"]
old-location: security\icenroll4_genkeyflags.htm
tech.root: security
ms.assetid: d22fe4d4-a939-4f77-8e11-f9312c81ec1e
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],GenKeyFlags property, GenKeyFlags property [Security], GenKeyFlags property [Security],CEnroll object, GenKeyFlags property [Security],ICEnroll interface, GenKeyFlags property [Security],ICEnroll2 interface, GenKeyFlags property [Security],ICEnroll3 interface, GenKeyFlags property [Security],ICEnroll4 interface, ICEnroll interface [Security],GenKeyFlags property, ICEnroll.GenKeyFlags, ICEnroll.put_GenKeyFlags, ICEnroll2 interface [Security],GenKeyFlags property, ICEnroll2.GenKeyFlags, ICEnroll2::get_GenKeyFlags, ICEnroll2::put_GenKeyFlags, ICEnroll3 interface [Security],GenKeyFlags property, ICEnroll3.GenKeyFlags, ICEnroll3::get_GenKeyFlags, ICEnroll3::put_GenKeyFlags, ICEnroll4 interface [Security],GenKeyFlags property, ICEnroll4.GenKeyFlags, ICEnroll4::GenKeyFlags, ICEnroll4::get_GenKeyFlags, ICEnroll4::put_GenKeyFlags, ICEnroll::get_GenKeyFlags, ICEnroll::put_GenKeyFlags, put_GenKeyFlags, security.icenroll4_genkeyflags, xenroll/ICEnroll2::GenKeyFlags, xenroll/ICEnroll2::get_GenKeyFlags, xenroll/ICEnroll2::put_GenKeyFlags, xenroll/ICEnroll3::GenKeyFlags, xenroll/ICEnroll3::get_GenKeyFlags, xenroll/ICEnroll3::put_GenKeyFlags, xenroll/ICEnroll4::GenKeyFlags, xenroll/ICEnroll4::get_GenKeyFlags, xenroll/ICEnroll4::put_GenKeyFlags, xenroll/ICEnroll::GenKeyFlags, xenroll/ICEnroll::get_GenKeyFlags, xenroll/ICEnroll::put_GenKeyFlags
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
 - ICEnroll::put_GenKeyFlags
 - xenroll/ICEnroll::put_GenKeyFlags
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
 - ICEnroll4.GenKeyFlags
 - ICEnroll4.get_GenKeyFlags
 - ICEnroll4.put_GenKeyFlags
 - ICEnroll3.GenKeyFlags
 - ICEnroll3.get_GenKeyFlags
 - ICEnroll3.put_GenKeyFlags
 - ICEnroll2.GenKeyFlags
 - ICEnroll2.get_GenKeyFlags
 - ICEnroll2.put_GenKeyFlags
 - ICEnroll.GenKeyFlags
 - ICEnroll.get_GenKeyFlags
 - ICEnroll.put_GenKeyFlags
 - CEnroll.GenKeyFlags
---

# ICEnroll::put_GenKeyFlags


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GenKeyFlags</b> property sets or retrieves the values passed to the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>  function when the certificate request is generated.

By default, the <b>GenKeyFlags</b> property is set to zero. However, when a .pvk file is specified, the value of <b>GenKeyFlags</b> defaults to CRYPT_EXPORTABLE. For more information, see Remarks.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

By default, private keys are not exportable unless a .pvk file is requested. To make the private key exportable without specifying a .pvk file, set <b>GenKeyFlags</b> to CRYPT_EXPORTABLE.

To specify a .pvk file name,  use the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">PVKFileName</a> property.

The <b>GenKeyFlags</b> property value is passed to the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> CryptoAPI function by using its <i>dwFlags</i> parameter.

If the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a>  (CSP) does not support exportable private keys, an error occurs.


The <b>GenKeyFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-createrequest">createRequest</a>
</li>
</ul>


<div class="alert"><b>Note</b>  The default value for the <b>GenKeyFlags</b> property is zero. If you need to change this value, you must do so before calling these methods. After calling any of these methods, you cannot change the <b>GenKeyFlags</b> property value.</div>
<div> </div>

#### Examples


```cpp
LONG     lGenKey;
HRESULT  hr;

// pEnroll is a previously instantiated ICEnroll interface pointer.

// Get the GenKeyFlags value.
hr = pEnroll->get_GenKeyFlags( &lGenKey );
if (FAILED( hr ))
    printf("Failed get_GenKeyFlags - %x\n", hr );
else
    printf( "GenKeyFlags: %d\n", lGenKey );

// Set the GenKeyFlags value.
hr = pEnroll->put_GenKeyFlags( CRYPT_EXPORTABLE );
if (FAILED( hr ))
    printf("Failed put_GenKeyFlags - %x\n", hr );
else
    printf( "GenKeyFlags set to %d\n", CRYPT_EXPORTABLE );
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>
