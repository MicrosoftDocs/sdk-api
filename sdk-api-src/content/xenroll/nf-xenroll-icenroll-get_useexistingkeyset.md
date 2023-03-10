---
UID: NF:xenroll.ICEnroll.get_UseExistingKeySet
title: ICEnroll::get_UseExistingKeySet (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether the existing keys should be used. (Get)
helpviewer_keywords: ["CEnroll object [Security]","UseExistingKeySet property","ICEnroll interface [Security]","UseExistingKeySet property","ICEnroll.UseExistingKeySet","ICEnroll.get_UseExistingKeySet","ICEnroll2 interface [Security]","UseExistingKeySet property","ICEnroll2.UseExistingKeySet","ICEnroll2::get_UseExistingKeySet","ICEnroll2::put_UseExistingKeySet","ICEnroll3 interface [Security]","UseExistingKeySet property","ICEnroll3.UseExistingKeySet","ICEnroll3::get_UseExistingKeySet","ICEnroll3::put_UseExistingKeySet","ICEnroll4 interface [Security]","UseExistingKeySet property","ICEnroll4.UseExistingKeySet","ICEnroll4::UseExistingKeySet","ICEnroll4::get_UseExistingKeySet","ICEnroll4::put_UseExistingKeySet","ICEnroll::get_UseExistingKeySet","ICEnroll::put_UseExistingKeySet","UseExistingKeySet property [Security]","UseExistingKeySet property [Security]","CEnroll object","UseExistingKeySet property [Security]","ICEnroll interface","UseExistingKeySet property [Security]","ICEnroll2 interface","UseExistingKeySet property [Security]","ICEnroll3 interface","UseExistingKeySet property [Security]","ICEnroll4 interface","get_UseExistingKeySet","security.icenroll4_useexistingkeyset","xenroll/ICEnroll2::UseExistingKeySet","xenroll/ICEnroll2::get_UseExistingKeySet","xenroll/ICEnroll2::put_UseExistingKeySet","xenroll/ICEnroll3::UseExistingKeySet","xenroll/ICEnroll3::get_UseExistingKeySet","xenroll/ICEnroll3::put_UseExistingKeySet","xenroll/ICEnroll4::UseExistingKeySet","xenroll/ICEnroll4::get_UseExistingKeySet","xenroll/ICEnroll4::put_UseExistingKeySet","xenroll/ICEnroll::UseExistingKeySet","xenroll/ICEnroll::get_UseExistingKeySet","xenroll/ICEnroll::put_UseExistingKeySet"]
old-location: security\icenroll4_useexistingkeyset.htm
tech.root: security
ms.assetid: e5115033-bda1-4160-84b3-80c692bf64fb
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],UseExistingKeySet property, ICEnroll interface [Security],UseExistingKeySet property, ICEnroll.UseExistingKeySet, ICEnroll.get_UseExistingKeySet, ICEnroll2 interface [Security],UseExistingKeySet property, ICEnroll2.UseExistingKeySet, ICEnroll2::get_UseExistingKeySet, ICEnroll2::put_UseExistingKeySet, ICEnroll3 interface [Security],UseExistingKeySet property, ICEnroll3.UseExistingKeySet, ICEnroll3::get_UseExistingKeySet, ICEnroll3::put_UseExistingKeySet, ICEnroll4 interface [Security],UseExistingKeySet property, ICEnroll4.UseExistingKeySet, ICEnroll4::UseExistingKeySet, ICEnroll4::get_UseExistingKeySet, ICEnroll4::put_UseExistingKeySet, ICEnroll::get_UseExistingKeySet, ICEnroll::put_UseExistingKeySet, UseExistingKeySet property [Security], UseExistingKeySet property [Security],CEnroll object, UseExistingKeySet property [Security],ICEnroll interface, UseExistingKeySet property [Security],ICEnroll2 interface, UseExistingKeySet property [Security],ICEnroll3 interface, UseExistingKeySet property [Security],ICEnroll4 interface, get_UseExistingKeySet, security.icenroll4_useexistingkeyset, xenroll/ICEnroll2::UseExistingKeySet, xenroll/ICEnroll2::get_UseExistingKeySet, xenroll/ICEnroll2::put_UseExistingKeySet, xenroll/ICEnroll3::UseExistingKeySet, xenroll/ICEnroll3::get_UseExistingKeySet, xenroll/ICEnroll3::put_UseExistingKeySet, xenroll/ICEnroll4::UseExistingKeySet, xenroll/ICEnroll4::get_UseExistingKeySet, xenroll/ICEnroll4::put_UseExistingKeySet, xenroll/ICEnroll::UseExistingKeySet, xenroll/ICEnroll::get_UseExistingKeySet, xenroll/ICEnroll::put_UseExistingKeySet
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
 - ICEnroll::get_UseExistingKeySet
 - xenroll/ICEnroll::get_UseExistingKeySet
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
 - ICEnroll4.UseExistingKeySet
 - ICEnroll4.get_UseExistingKeySet
 - ICEnroll4.put_UseExistingKeySet
 - ICEnroll3.UseExistingKeySet
 - ICEnroll3.get_UseExistingKeySet
 - ICEnroll3.put_UseExistingKeySet
 - ICEnroll2.UseExistingKeySet
 - ICEnroll2.get_UseExistingKeySet
 - ICEnroll2.put_UseExistingKeySet
 - ICEnroll.UseExistingKeySet
 - ICEnroll.get_UseExistingKeySet
 - ICEnroll.put_UseExistingKeySet
 - CEnroll.UseExistingKeySet
---

# ICEnroll::get_UseExistingKeySet


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>UseExistingKeySet</b> property sets or retrieves a Boolean value that determines whether the existing keys should be used.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

 If an existing key set is used, the <b>UseExistingKeySet</b> property must be set to true.


The <b>UseExistingKeySet</b> property affects the behavior of the following methods:

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
BOOL     bUEKS;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the UseExistingKeySet value
hr = pEnroll->get_UseExistingKeySet( &bUEKS );
if (FAILED( hr ))
    printf("Failed get_UseExistingKeySet - %x\n", hr );
else
    printf( "UseExistingKeySet: %d\n", bUEKS );

// set the UseExistingKeySet value
hr = pEnroll->put_UseExistingKeySet( TRUE );
if (FAILED( hr ))
    printf("Failed put_UseExistingKeySet - %x\n", hr );
else
    printf( "UseExistingKeySet set to TRUE\n" );
```
