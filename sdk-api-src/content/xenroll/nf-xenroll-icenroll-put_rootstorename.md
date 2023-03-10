---
UID: NF:xenroll.ICEnroll.put_RootStoreName
title: ICEnroll::put_RootStoreName (xenroll.h)
description: Sets or retrieves the name of the root store where all intrinsically trusted, self-signed root certificates are kept. (Put)
helpviewer_keywords: ["CEnroll object [Security]","RootStoreName property","ICEnroll interface [Security]","RootStoreName property","ICEnroll.RootStoreName","ICEnroll.put_RootStoreName","ICEnroll2 interface [Security]","RootStoreName property","ICEnroll2.RootStoreName","ICEnroll2::get_RootStoreName","ICEnroll2::put_RootStoreName","ICEnroll3 interface [Security]","RootStoreName property","ICEnroll3.RootStoreName","ICEnroll3::get_RootStoreName","ICEnroll3::put_RootStoreName","ICEnroll4 interface [Security]","RootStoreName property","ICEnroll4.RootStoreName","ICEnroll4::RootStoreName","ICEnroll4::get_RootStoreName","ICEnroll4::put_RootStoreName","ICEnroll::get_RootStoreName","ICEnroll::put_RootStoreName","RootStoreName property [Security]","RootStoreName property [Security]","CEnroll object","RootStoreName property [Security]","ICEnroll interface","RootStoreName property [Security]","ICEnroll2 interface","RootStoreName property [Security]","ICEnroll3 interface","RootStoreName property [Security]","ICEnroll4 interface","put_RootStoreName","security.icenroll4_rootstorename","xenroll/ICEnroll2::RootStoreName","xenroll/ICEnroll2::get_RootStoreName","xenroll/ICEnroll2::put_RootStoreName","xenroll/ICEnroll3::RootStoreName","xenroll/ICEnroll3::get_RootStoreName","xenroll/ICEnroll3::put_RootStoreName","xenroll/ICEnroll4::RootStoreName","xenroll/ICEnroll4::get_RootStoreName","xenroll/ICEnroll4::put_RootStoreName","xenroll/ICEnroll::RootStoreName","xenroll/ICEnroll::get_RootStoreName","xenroll/ICEnroll::put_RootStoreName"]
old-location: security\icenroll4_rootstorename.htm
tech.root: security
ms.assetid: 5b686ade-e8ee-4c59-ab90-05088f575acd
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],RootStoreName property, ICEnroll interface [Security],RootStoreName property, ICEnroll.RootStoreName, ICEnroll.put_RootStoreName, ICEnroll2 interface [Security],RootStoreName property, ICEnroll2.RootStoreName, ICEnroll2::get_RootStoreName, ICEnroll2::put_RootStoreName, ICEnroll3 interface [Security],RootStoreName property, ICEnroll3.RootStoreName, ICEnroll3::get_RootStoreName, ICEnroll3::put_RootStoreName, ICEnroll4 interface [Security],RootStoreName property, ICEnroll4.RootStoreName, ICEnroll4::RootStoreName, ICEnroll4::get_RootStoreName, ICEnroll4::put_RootStoreName, ICEnroll::get_RootStoreName, ICEnroll::put_RootStoreName, RootStoreName property [Security], RootStoreName property [Security],CEnroll object, RootStoreName property [Security],ICEnroll interface, RootStoreName property [Security],ICEnroll2 interface, RootStoreName property [Security],ICEnroll3 interface, RootStoreName property [Security],ICEnroll4 interface, put_RootStoreName, security.icenroll4_rootstorename, xenroll/ICEnroll2::RootStoreName, xenroll/ICEnroll2::get_RootStoreName, xenroll/ICEnroll2::put_RootStoreName, xenroll/ICEnroll3::RootStoreName, xenroll/ICEnroll3::get_RootStoreName, xenroll/ICEnroll3::put_RootStoreName, xenroll/ICEnroll4::RootStoreName, xenroll/ICEnroll4::get_RootStoreName, xenroll/ICEnroll4::put_RootStoreName, xenroll/ICEnroll::RootStoreName, xenroll/ICEnroll::get_RootStoreName, xenroll/ICEnroll::put_RootStoreName
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
 - ICEnroll::put_RootStoreName
 - xenroll/ICEnroll::put_RootStoreName
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
 - ICEnroll4.RootStoreName
 - ICEnroll4.get_RootStoreName
 - ICEnroll4.put_RootStoreName
 - ICEnroll3.RootStoreName
 - ICEnroll3.get_RootStoreName
 - ICEnroll3.put_RootStoreName
 - ICEnroll2.RootStoreName
 - ICEnroll2.get_RootStoreName
 - ICEnroll2.put_RootStoreName
 - ICEnroll.RootStoreName
 - ICEnroll.get_RootStoreName
 - ICEnroll.put_RootStoreName
 - CEnroll.RootStoreName
---

# ICEnroll::put_RootStoreName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreName</b> property sets or retrieves the name of the root store where all intrinsically trusted, self-signed <a href="/windows/desktop/SecGloss/r-gly">root certificates</a> are kept.

 The default value for this property is "ROOT". Because of the level of trust associated with the root store, the user may be prompted (by means of the user interface) to accept the certificate. Although this property need not be changed for many applications, to avoid the user interface associated with trusting <a href="/windows/desktop/SecGloss/r-gly">root certificates</a>, a possibility is to set <b>RootStoreName</b> to "CA".

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

<b>RootStoreName</b> affects the behavior of the following methods:

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
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storename
hr = pEnroll->get_RootStoreName( &bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting RootStoreName - %x\n", hr );
else
    printf( "RootStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName is a BSTR that is previously set to a valid store name
hr = pEnroll->put_RootStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting RootStoreName - %x\n", hr );
else
    printf( "RootStoreName was set to : %ws\n", bstrNewName );
```
