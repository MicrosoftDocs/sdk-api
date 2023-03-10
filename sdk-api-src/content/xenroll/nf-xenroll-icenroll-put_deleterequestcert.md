---
UID: NF:xenroll.ICEnroll.put_DeleteRequestCert
title: ICEnroll::put_DeleteRequestCert (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether dummy certificates in the request store are deleted. (Put)
helpviewer_keywords: ["CEnroll object [Security]","DeleteRequestCert property","DeleteRequestCert property [Security]","DeleteRequestCert property [Security]","CEnroll object","DeleteRequestCert property [Security]","ICEnroll interface","DeleteRequestCert property [Security]","ICEnroll2 interface","DeleteRequestCert property [Security]","ICEnroll3 interface","DeleteRequestCert property [Security]","ICEnroll4 interface","ICEnroll interface [Security]","DeleteRequestCert property","ICEnroll.DeleteRequestCert","ICEnroll.put_DeleteRequestCert","ICEnroll2 interface [Security]","DeleteRequestCert property","ICEnroll2.DeleteRequestCert","ICEnroll2::get_DeleteRequestCert","ICEnroll2::put_DeleteRequestCert","ICEnroll3 interface [Security]","DeleteRequestCert property","ICEnroll3.DeleteRequestCert","ICEnroll3::get_DeleteRequestCert","ICEnroll3::put_DeleteRequestCert","ICEnroll4 interface [Security]","DeleteRequestCert property","ICEnroll4.DeleteRequestCert","ICEnroll4::DeleteRequestCert","ICEnroll4::get_DeleteRequestCert","ICEnroll4::put_DeleteRequestCert","ICEnroll::get_DeleteRequestCert","ICEnroll::put_DeleteRequestCert","put_DeleteRequestCert","security.icenroll4_deleterequestcert","xenroll/ICEnroll2::DeleteRequestCert","xenroll/ICEnroll2::get_DeleteRequestCert","xenroll/ICEnroll2::put_DeleteRequestCert","xenroll/ICEnroll3::DeleteRequestCert","xenroll/ICEnroll3::get_DeleteRequestCert","xenroll/ICEnroll3::put_DeleteRequestCert","xenroll/ICEnroll4::DeleteRequestCert","xenroll/ICEnroll4::get_DeleteRequestCert","xenroll/ICEnroll4::put_DeleteRequestCert","xenroll/ICEnroll::DeleteRequestCert","xenroll/ICEnroll::get_DeleteRequestCert","xenroll/ICEnroll::put_DeleteRequestCert"]
old-location: security\icenroll4_deleterequestcert.htm
tech.root: security
ms.assetid: f026f4ed-e003-4ece-8c08-427dac48229f
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],DeleteRequestCert property, DeleteRequestCert property [Security], DeleteRequestCert property [Security],CEnroll object, DeleteRequestCert property [Security],ICEnroll interface, DeleteRequestCert property [Security],ICEnroll2 interface, DeleteRequestCert property [Security],ICEnroll3 interface, DeleteRequestCert property [Security],ICEnroll4 interface, ICEnroll interface [Security],DeleteRequestCert property, ICEnroll.DeleteRequestCert, ICEnroll.put_DeleteRequestCert, ICEnroll2 interface [Security],DeleteRequestCert property, ICEnroll2.DeleteRequestCert, ICEnroll2::get_DeleteRequestCert, ICEnroll2::put_DeleteRequestCert, ICEnroll3 interface [Security],DeleteRequestCert property, ICEnroll3.DeleteRequestCert, ICEnroll3::get_DeleteRequestCert, ICEnroll3::put_DeleteRequestCert, ICEnroll4 interface [Security],DeleteRequestCert property, ICEnroll4.DeleteRequestCert, ICEnroll4::DeleteRequestCert, ICEnroll4::get_DeleteRequestCert, ICEnroll4::put_DeleteRequestCert, ICEnroll::get_DeleteRequestCert, ICEnroll::put_DeleteRequestCert, put_DeleteRequestCert, security.icenroll4_deleterequestcert, xenroll/ICEnroll2::DeleteRequestCert, xenroll/ICEnroll2::get_DeleteRequestCert, xenroll/ICEnroll2::put_DeleteRequestCert, xenroll/ICEnroll3::DeleteRequestCert, xenroll/ICEnroll3::get_DeleteRequestCert, xenroll/ICEnroll3::put_DeleteRequestCert, xenroll/ICEnroll4::DeleteRequestCert, xenroll/ICEnroll4::get_DeleteRequestCert, xenroll/ICEnroll4::put_DeleteRequestCert, xenroll/ICEnroll::DeleteRequestCert, xenroll/ICEnroll::get_DeleteRequestCert, xenroll/ICEnroll::put_DeleteRequestCert
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
 - ICEnroll::put_DeleteRequestCert
 - xenroll/ICEnroll::put_DeleteRequestCert
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
 - ICEnroll4.DeleteRequestCert
 - ICEnroll4.get_DeleteRequestCert
 - ICEnroll4.put_DeleteRequestCert
 - ICEnroll3.DeleteRequestCert
 - ICEnroll3.get_DeleteRequestCert
 - ICEnroll3.put_DeleteRequestCert
 - ICEnroll2.DeleteRequestCert
 - ICEnroll2.get_DeleteRequestCert
 - ICEnroll2.put_DeleteRequestCert
 - ICEnroll.DeleteRequestCert
 - ICEnroll.get_DeleteRequestCert
 - ICEnroll.put_DeleteRequestCert
 - CEnroll.DeleteRequestCert
---

# ICEnroll::put_DeleteRequestCert


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>DeleteRequestCert</b> property sets or retrieves a Boolean value that  determines whether dummy certificates in the request store are deleted.

Dummy certificates are created for the purpose of persisting the keys generated for the PKCS #10 request during the enrollment process. The store specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a> property is where the dummy certificate is created. The newly generated keys are added as properties to the dummy certificate to persist them until a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> processes the request and responds with a PKCS #7. On acceptance of the PKCS #7, the dummy certificate is removed and the keys are added as properties of the issued certificate returned by the certification authority. For debugging and testing, it is often desirable to not delete the dummy certificate. Setting the <b>DeleteRequestCert</b> property to <b>FALSE</b> prevents its deletion.

The default value for this property is  <b>TRUE</b>. This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>DeleteRequestCert</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
</li>
</ul>



#### Examples


```cpp
BOOL     bDRC;
HRESULT  hr;


// pEnroll is a previously instantiated ICEnroll interface pointer.
// Get the DeleteRequestCert Boolean value.

hr = pEnroll->get_DeleteRequestCert( &bDRC );
if ( FAILED ( hr ) )
    printf("Failed getting DeleteRequestCert - %x\n", hr );
else
    printf( "DeleteRequestCert: %s\n", ( bDRC ? "TRUE" : "FALSE" ) );


// Set the DeleteRequestCert value.

hr = pEnroll->put_DeleteRequestCert( FALSE );
if ( FAILED ( hr ) )
    printf("Failed Setting DeleteRequestCert - %x\n", hr );
else
    printf( "DeleteRequestCert was set to FALSE\n" );
```
