---
UID: NF:xenroll.ICEnroll.get_CAStoreName
title: ICEnroll::get_CAStoreName (xenroll.h)
description: Sets or retrieves the name of the store where all non-&quot;ROOT&quot; and non-&quot;MY&quot; certificates are kept. (Get)
helpviewer_keywords: ["CAStoreName property [Security]","CAStoreName property [Security]","CEnroll object","CAStoreName property [Security]","ICEnroll interface","CAStoreName property [Security]","ICEnroll2 interface","CAStoreName property [Security]","ICEnroll3 interface","CAStoreName property [Security]","ICEnroll4 interface","CEnroll object [Security]","CAStoreName property","ICEnroll interface [Security]","CAStoreName property","ICEnroll.CAStoreName","ICEnroll.get_CAStoreName","ICEnroll2 interface [Security]","CAStoreName property","ICEnroll2.CAStoreName","ICEnroll2::get_CAStoreName","ICEnroll2::put_CAStoreName","ICEnroll3 interface [Security]","CAStoreName property","ICEnroll3.CAStoreName","ICEnroll3::get_CAStoreName","ICEnroll3::put_CAStoreName","ICEnroll4 interface [Security]","CAStoreName property","ICEnroll4.CAStoreName","ICEnroll4::CAStoreName","ICEnroll4::get_CAStoreName","ICEnroll4::put_CAStoreName","ICEnroll::get_CAStoreName","ICEnroll::put_CAStoreName","get_CAStoreName","security.icenroll4_castorename","xenroll/ICEnroll2::CAStoreName","xenroll/ICEnroll2::get_CAStoreName","xenroll/ICEnroll2::put_CAStoreName","xenroll/ICEnroll3::CAStoreName","xenroll/ICEnroll3::get_CAStoreName","xenroll/ICEnroll3::put_CAStoreName","xenroll/ICEnroll4::CAStoreName","xenroll/ICEnroll4::get_CAStoreName","xenroll/ICEnroll4::put_CAStoreName","xenroll/ICEnroll::CAStoreName","xenroll/ICEnroll::get_CAStoreName","xenroll/ICEnroll::put_CAStoreName"]
old-location: security\icenroll4_castorename.htm
tech.root: security
ms.assetid: 29616175-7195-430e-a85b-99b50e276e7f
ms.date: 12/05/2018
ms.keywords: CAStoreName property [Security], CAStoreName property [Security],CEnroll object, CAStoreName property [Security],ICEnroll interface, CAStoreName property [Security],ICEnroll2 interface, CAStoreName property [Security],ICEnroll3 interface, CAStoreName property [Security],ICEnroll4 interface, CEnroll object [Security],CAStoreName property, ICEnroll interface [Security],CAStoreName property, ICEnroll.CAStoreName, ICEnroll.get_CAStoreName, ICEnroll2 interface [Security],CAStoreName property, ICEnroll2.CAStoreName, ICEnroll2::get_CAStoreName, ICEnroll2::put_CAStoreName, ICEnroll3 interface [Security],CAStoreName property, ICEnroll3.CAStoreName, ICEnroll3::get_CAStoreName, ICEnroll3::put_CAStoreName, ICEnroll4 interface [Security],CAStoreName property, ICEnroll4.CAStoreName, ICEnroll4::CAStoreName, ICEnroll4::get_CAStoreName, ICEnroll4::put_CAStoreName, ICEnroll::get_CAStoreName, ICEnroll::put_CAStoreName, get_CAStoreName, security.icenroll4_castorename, xenroll/ICEnroll2::CAStoreName, xenroll/ICEnroll2::get_CAStoreName, xenroll/ICEnroll2::put_CAStoreName, xenroll/ICEnroll3::CAStoreName, xenroll/ICEnroll3::get_CAStoreName, xenroll/ICEnroll3::put_CAStoreName, xenroll/ICEnroll4::CAStoreName, xenroll/ICEnroll4::get_CAStoreName, xenroll/ICEnroll4::put_CAStoreName, xenroll/ICEnroll::CAStoreName, xenroll/ICEnroll::get_CAStoreName, xenroll/ICEnroll::put_CAStoreName
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
 - ICEnroll::get_CAStoreName
 - xenroll/ICEnroll::get_CAStoreName
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
 - ICEnroll4.CAStoreName
 - ICEnroll4.get_CAStoreName
 - ICEnroll4.put_CAStoreName
 - ICEnroll3.CAStoreName
 - ICEnroll3.get_CAStoreName
 - ICEnroll3.put_CAStoreName
 - ICEnroll2.CAStoreName
 - ICEnroll2.get_CAStoreName
 - ICEnroll2.put_CAStoreName
 - ICEnroll.CAStoreName
 - ICEnroll.get_CAStoreName
 - ICEnroll.put_CAStoreName
 - CEnroll.CAStoreName
---

# ICEnroll::get_CAStoreName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreName</b> property sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.

The default value for this property is "CA". This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>CAStoreName</b> property affects the behavior of the following methods:

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
hr = pEnroll->get_CAStoreName( &bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting CAStoreName - %x\n", hr );
else
    printf( "CAStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting CAStoreName - %x\n", hr );
else
    printf( "CAStoreName was set to : %ws\n", bstrNewName );
```
