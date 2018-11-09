---
UID: NF:xenroll.ICEnroll.get_RequestStoreName
title: ICEnroll::get_RequestStoreName
author: windows-sdk-content
description: Sets or retrievesICEnroll the name of the store that contains the dummy certificate.
old-location: security\icenroll4_requeststorename.htm
tech.root: seccrypto
ms.assetid: c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CEnroll object [Security],RequestStoreName property, ICEnroll interface [Security],RequestStoreName property, ICEnroll.RequestStoreName, ICEnroll.get_RequestStoreName, ICEnroll2 interface [Security],RequestStoreName property, ICEnroll2.RequestStoreName, ICEnroll2::get_RequestStoreName, ICEnroll2::put_RequestStoreName, ICEnroll3 interface [Security],RequestStoreName property, ICEnroll3.RequestStoreName, ICEnroll3::get_RequestStoreName, ICEnroll3::put_RequestStoreName, ICEnroll4 interface [Security],RequestStoreName property, ICEnroll4.RequestStoreName, ICEnroll4::RequestStoreName, ICEnroll4::get_RequestStoreName, ICEnroll4::put_RequestStoreName, ICEnroll::get_RequestStoreName, ICEnroll::put_RequestStoreName, RequestStoreName property [Security], RequestStoreName property [Security],CEnroll object, RequestStoreName property [Security],ICEnroll interface, RequestStoreName property [Security],ICEnroll2 interface, RequestStoreName property [Security],ICEnroll3 interface, RequestStoreName property [Security],ICEnroll4 interface, get_RequestStoreName, security.icenroll4_requeststorename, xenroll/ICEnroll2::RequestStoreName, xenroll/ICEnroll2::get_RequestStoreName, xenroll/ICEnroll2::put_RequestStoreName, xenroll/ICEnroll3::RequestStoreName, xenroll/ICEnroll3::get_RequestStoreName, xenroll/ICEnroll3::put_RequestStoreName, xenroll/ICEnroll4::RequestStoreName, xenroll/ICEnroll4::get_RequestStoreName, xenroll/ICEnroll4::put_RequestStoreName, xenroll/ICEnroll::RequestStoreName, xenroll/ICEnroll::get_RequestStoreName, xenroll/ICEnroll::put_RequestStoreName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.RequestStoreName
 - ICEnroll4.get_RequestStoreName
 - ICEnroll4.put_RequestStoreName
 - ICEnroll3.RequestStoreName
 - ICEnroll3.get_RequestStoreName
 - ICEnroll3.put_RequestStoreName
 - ICEnroll2.RequestStoreName
 - ICEnroll2.get_RequestStoreName
 - ICEnroll2.put_RequestStoreName
 - ICEnroll.RequestStoreName
 - ICEnroll.get_RequestStoreName
 - ICEnroll.put_RequestStoreName
 - CEnroll.RequestStoreName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::get_RequestStoreName


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreName</b> property sets or retrieves<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> processes the request and responds with a PKCS #7.

The default value for this property is  "REQUEST". If the default is not to be used, this property must be set to the store to be used before calls to 
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a> or <a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a> and again before calls to 
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a> or <a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>.

This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



Typically, modification of the <b>RequestStoreName</b> property is  performed only in advanced applications. Changing this value is not recommended for most applications.


The <b>RequestStoreName</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
</ul>


The ability to set this property is disabled when  the Certificate Enrollment Control is executed as a scripted control.


#### Examples


```cpp
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storename
hr = pEnroll->get_RequestStoreName( &bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting RequestStoreName - %x\n", hr );
else
    printf( "RequestStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName is a BSTR that is previously set to a valid store name
hr = pEnroll->put_RequestStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting RequestStoreName - %x\n", hr );
else
    printf( "RequestStoreName was set to : %ws\n", bstrNewName );
```




