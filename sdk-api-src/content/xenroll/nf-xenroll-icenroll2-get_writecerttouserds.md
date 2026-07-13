---
UID: NF:xenroll.ICEnroll2.get_WriteCertToUserDS
title: ICEnroll2::get_WriteCertToUserDS (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory store. (Get)
helpviewer_keywords: ["CEnroll object [Security]","WriteCertToUserDS property","ICEnroll2 interface [Security]","WriteCertToUserDS property","ICEnroll2.WriteCertToUserDS","ICEnroll2.get_WriteCertToUserDS","ICEnroll2::get_WriteCertToUserDS","ICEnroll2::put_WriteCertToUserDS","ICEnroll3 interface [Security]","WriteCertToUserDS property","ICEnroll3.WriteCertToUserDS","ICEnroll3::get_WriteCertToUserDS","ICEnroll3::put_WriteCertToUserDS","ICEnroll4 interface [Security]","WriteCertToUserDS property","ICEnroll4.WriteCertToUserDS","ICEnroll4::WriteCertToUserDS","ICEnroll4::get_WriteCertToUserDS","ICEnroll4::put_WriteCertToUserDS","WriteCertToUserDS property [Security]","WriteCertToUserDS property [Security]","CEnroll object","WriteCertToUserDS property [Security]","ICEnroll2 interface","WriteCertToUserDS property [Security]","ICEnroll3 interface","WriteCertToUserDS property [Security]","ICEnroll4 interface","get_WriteCertToUserDS","security.icenroll4_writecerttouserds","xenroll/ICEnroll2::WriteCertToUserDS","xenroll/ICEnroll2::get_WriteCertToUserDS","xenroll/ICEnroll2::put_WriteCertToUserDS","xenroll/ICEnroll3::WriteCertToUserDS","xenroll/ICEnroll3::get_WriteCertToUserDS","xenroll/ICEnroll3::put_WriteCertToUserDS","xenroll/ICEnroll4::WriteCertToUserDS","xenroll/ICEnroll4::get_WriteCertToUserDS","xenroll/ICEnroll4::put_WriteCertToUserDS"]
old-location: security\icenroll4_writecerttouserds.htm
tech.root: security
ms.assetid: 8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],WriteCertToUserDS property, ICEnroll2 interface [Security],WriteCertToUserDS property, ICEnroll2.WriteCertToUserDS, ICEnroll2.get_WriteCertToUserDS, ICEnroll2::get_WriteCertToUserDS, ICEnroll2::put_WriteCertToUserDS, ICEnroll3 interface [Security],WriteCertToUserDS property, ICEnroll3.WriteCertToUserDS, ICEnroll3::get_WriteCertToUserDS, ICEnroll3::put_WriteCertToUserDS, ICEnroll4 interface [Security],WriteCertToUserDS property, ICEnroll4.WriteCertToUserDS, ICEnroll4::WriteCertToUserDS, ICEnroll4::get_WriteCertToUserDS, ICEnroll4::put_WriteCertToUserDS, WriteCertToUserDS property [Security], WriteCertToUserDS property [Security],CEnroll object, WriteCertToUserDS property [Security],ICEnroll2 interface, WriteCertToUserDS property [Security],ICEnroll3 interface, WriteCertToUserDS property [Security],ICEnroll4 interface, get_WriteCertToUserDS, security.icenroll4_writecerttouserds, xenroll/ICEnroll2::WriteCertToUserDS, xenroll/ICEnroll2::get_WriteCertToUserDS, xenroll/ICEnroll2::put_WriteCertToUserDS, xenroll/ICEnroll3::WriteCertToUserDS, xenroll/ICEnroll3::get_WriteCertToUserDS, xenroll/ICEnroll3::put_WriteCertToUserDS, xenroll/ICEnroll4::WriteCertToUserDS, xenroll/ICEnroll4::get_WriteCertToUserDS, xenroll/ICEnroll4::put_WriteCertToUserDS
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
 - ICEnroll2::get_WriteCertToUserDS
 - xenroll/ICEnroll2::get_WriteCertToUserDS
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
 - ICEnroll4.WriteCertToUserDS
 - ICEnroll4.get_WriteCertToUserDS
 - ICEnroll4.put_WriteCertToUserDS
 - ICEnroll3.WriteCertToUserDS
 - ICEnroll3.get_WriteCertToUserDS
 - ICEnroll3.put_WriteCertToUserDS
 - ICEnroll2.WriteCertToUserDS
 - ICEnroll2.get_WriteCertToUserDS
 - ICEnroll2.put_WriteCertToUserDS
 - CEnroll.WriteCertToUserDS
---

# ICEnroll2::get_WriteCertToUserDS


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToUserDS</b> property sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory  store.

 This property should not need to be modified by most applications. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

<b>WriteCertToUserDS</b> affects the behavior of the following methods:

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
BOOL     bWriteUserDS;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll2 interface pointer

// get the WriteCertToUserDS value
hr = pEnroll->get_WriteCertToUserDS( &bWriteUserDS );
if (FAILED( hr ))
    printf("Failed get_WriteCertToUserDS - %x\n", hr );
else
    printf( "WriteCertToUserDS: %d\n", bWriteUserDS );

// set the WriteCertToUserDS value
hr = pEnroll->put_WriteCertToUserDS( TRUE );
if (FAILED( hr ))
    printf("Failed put_WriteCertToUserDS - %x\n", hr );
else
    printf( "WriteCertToUserDS set to TRUE\n" );
```
