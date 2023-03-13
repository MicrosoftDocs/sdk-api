---
UID: NF:xenroll.ICEnroll2.put_EnableT61DNEncoding
title: ICEnroll2::put_EnableT61DNEncoding (xenroll.h)
description: The EnableT61DNEncoding property of ICEnroll4 sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a Unicode string. (Put)
helpviewer_keywords: ["CEnroll object [Security]","EnableT61DNEncoding property","EnableT61DNEncoding property [Security]","EnableT61DNEncoding property [Security]","CEnroll object","EnableT61DNEncoding property [Security]","ICEnroll2 interface","EnableT61DNEncoding property [Security]","ICEnroll3 interface","EnableT61DNEncoding property [Security]","ICEnroll4 interface","ICEnroll2 interface [Security]","EnableT61DNEncoding property","ICEnroll2.EnableT61DNEncoding","ICEnroll2.put_EnableT61DNEncoding","ICEnroll2::get_EnableT61DNEncoding","ICEnroll2::put_EnableT61DNEncoding","ICEnroll3 interface [Security]","EnableT61DNEncoding property","ICEnroll3.EnableT61DNEncoding","ICEnroll3::get_EnableT61DNEncoding","ICEnroll3::put_EnableT61DNEncoding","ICEnroll4 interface [Security]","EnableT61DNEncoding property","ICEnroll4.EnableT61DNEncoding","ICEnroll4::EnableT61DNEncoding","ICEnroll4::get_EnableT61DNEncoding","ICEnroll4::put_EnableT61DNEncoding","put_EnableT61DNEncoding","security.icenroll4_enablet61dnencoding","xenroll/ICEnroll2::EnableT61DNEncoding","xenroll/ICEnroll2::get_EnableT61DNEncoding","xenroll/ICEnroll2::put_EnableT61DNEncoding","xenroll/ICEnroll3::EnableT61DNEncoding","xenroll/ICEnroll3::get_EnableT61DNEncoding","xenroll/ICEnroll3::put_EnableT61DNEncoding","xenroll/ICEnroll4::EnableT61DNEncoding","xenroll/ICEnroll4::get_EnableT61DNEncoding","xenroll/ICEnroll4::put_EnableT61DNEncoding"]
old-location: security\icenroll4_enablet61dnencoding.htm
tech.root: security
ms.assetid: ff8fe103-0303-4f40-af25-efa50155c36f
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],EnableT61DNEncoding property, EnableT61DNEncoding property [Security], EnableT61DNEncoding property [Security],CEnroll object, EnableT61DNEncoding property [Security],ICEnroll2 interface, EnableT61DNEncoding property [Security],ICEnroll3 interface, EnableT61DNEncoding property [Security],ICEnroll4 interface, ICEnroll2 interface [Security],EnableT61DNEncoding property, ICEnroll2.EnableT61DNEncoding, ICEnroll2.put_EnableT61DNEncoding, ICEnroll2::get_EnableT61DNEncoding, ICEnroll2::put_EnableT61DNEncoding, ICEnroll3 interface [Security],EnableT61DNEncoding property, ICEnroll3.EnableT61DNEncoding, ICEnroll3::get_EnableT61DNEncoding, ICEnroll3::put_EnableT61DNEncoding, ICEnroll4 interface [Security],EnableT61DNEncoding property, ICEnroll4.EnableT61DNEncoding, ICEnroll4::EnableT61DNEncoding, ICEnroll4::get_EnableT61DNEncoding, ICEnroll4::put_EnableT61DNEncoding, put_EnableT61DNEncoding, security.icenroll4_enablet61dnencoding, xenroll/ICEnroll2::EnableT61DNEncoding, xenroll/ICEnroll2::get_EnableT61DNEncoding, xenroll/ICEnroll2::put_EnableT61DNEncoding, xenroll/ICEnroll3::EnableT61DNEncoding, xenroll/ICEnroll3::get_EnableT61DNEncoding, xenroll/ICEnroll3::put_EnableT61DNEncoding, xenroll/ICEnroll4::EnableT61DNEncoding, xenroll/ICEnroll4::get_EnableT61DNEncoding, xenroll/ICEnroll4::put_EnableT61DNEncoding
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
 - ICEnroll2::put_EnableT61DNEncoding
 - xenroll/ICEnroll2::put_EnableT61DNEncoding
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
 - ICEnroll4.EnableT61DNEncoding
 - ICEnroll4.get_EnableT61DNEncoding
 - ICEnroll4.put_EnableT61DNEncoding
 - ICEnroll3.EnableT61DNEncoding
 - ICEnroll3.get_EnableT61DNEncoding
 - ICEnroll3.put_EnableT61DNEncoding
 - ICEnroll2.EnableT61DNEncoding
 - ICEnroll2.get_EnableT61DNEncoding
 - ICEnroll2.put_EnableT61DNEncoding
 - CEnroll.EnableT61DNEncoding
---

# ICEnroll2::put_EnableT61DNEncoding


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnableT61DNEncoding</b> property sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string.

 A T61 character is 8 bits, hence all Unicode characters to be encoded must be less than or equal to 0xFF.  This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>EnableT61DNEncoding</b> property affects the behavior of the following methods:

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
BOOL     bT61DN;
HRESULT  hr;


// pEnroll is a previously instantiated ICEnroll2 interface pointer.
// Get the EnableT61DNEncoding Boolean value.

hr = pEnroll->get_EnableT61DNEncoding( &bT61DN );
if ( FAILED ( hr ) )
    printf("Failed get_EnableT61DNEncoding - %x\n", hr );
else
    printf( "T61DNEncoding: %s\n", 
             ( bT61DN ? "Enabled" : "Disabled" ) );


// Set the EnableT61DNEncoding value.

hr = pEnroll->put_EnableT61DNEncoding( TRUE );
if ( FAILED ( hr ) )
    printf("Failed Setting EnableT61DNEncoding - %x\n", hr );
else
    printf( "EnableT61DNEncoding was set to TRUE\n" );
```
