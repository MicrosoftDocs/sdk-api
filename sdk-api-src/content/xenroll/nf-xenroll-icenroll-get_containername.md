---
UID: NF:xenroll.ICEnroll.get_ContainerName
title: ICEnroll::get_ContainerName (xenroll.h)
description: The ContainerName property of ICEnroll4 sets or retrieves the name of the key container to use. (Get)
helpviewer_keywords: ["CEnroll object [Security]","ContainerName property","ContainerName property [Security]","ContainerName property [Security]","CEnroll object","ContainerName property [Security]","ICEnroll interface","ContainerName property [Security]","ICEnroll2 interface","ContainerName property [Security]","ICEnroll3 interface","ContainerName property [Security]","ICEnroll4 interface","ICEnroll interface [Security]","ContainerName property","ICEnroll.ContainerName","ICEnroll.get_ContainerName","ICEnroll2 interface [Security]","ContainerName property","ICEnroll2.ContainerName","ICEnroll2::get_ContainerName","ICEnroll2::put_ContainerName","ICEnroll3 interface [Security]","ContainerName property","ICEnroll3.ContainerName","ICEnroll3::get_ContainerName","ICEnroll3::put_ContainerName","ICEnroll4 interface [Security]","ContainerName property","ICEnroll4.ContainerName","ICEnroll4::ContainerName","ICEnroll4::get_ContainerName","ICEnroll4::put_ContainerName","ICEnroll::get_ContainerName","ICEnroll::put_ContainerName","get_ContainerName","security.icenroll4_containername","xenroll/ICEnroll2::ContainerName","xenroll/ICEnroll2::get_ContainerName","xenroll/ICEnroll2::put_ContainerName","xenroll/ICEnroll3::ContainerName","xenroll/ICEnroll3::get_ContainerName","xenroll/ICEnroll3::put_ContainerName","xenroll/ICEnroll4::ContainerName","xenroll/ICEnroll4::get_ContainerName","xenroll/ICEnroll4::put_ContainerName","xenroll/ICEnroll::ContainerName","xenroll/ICEnroll::get_ContainerName","xenroll/ICEnroll::put_ContainerName"]
old-location: security\icenroll4_containername.htm
tech.root: security
ms.assetid: fa863843-8bbc-47c5-9d58-b64fb6703c0a
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],ContainerName property, ContainerName property [Security], ContainerName property [Security],CEnroll object, ContainerName property [Security],ICEnroll interface, ContainerName property [Security],ICEnroll2 interface, ContainerName property [Security],ICEnroll3 interface, ContainerName property [Security],ICEnroll4 interface, ICEnroll interface [Security],ContainerName property, ICEnroll.ContainerName, ICEnroll.get_ContainerName, ICEnroll2 interface [Security],ContainerName property, ICEnroll2.ContainerName, ICEnroll2::get_ContainerName, ICEnroll2::put_ContainerName, ICEnroll3 interface [Security],ContainerName property, ICEnroll3.ContainerName, ICEnroll3::get_ContainerName, ICEnroll3::put_ContainerName, ICEnroll4 interface [Security],ContainerName property, ICEnroll4.ContainerName, ICEnroll4::ContainerName, ICEnroll4::get_ContainerName, ICEnroll4::put_ContainerName, ICEnroll::get_ContainerName, ICEnroll::put_ContainerName, get_ContainerName, security.icenroll4_containername, xenroll/ICEnroll2::ContainerName, xenroll/ICEnroll2::get_ContainerName, xenroll/ICEnroll2::put_ContainerName, xenroll/ICEnroll3::ContainerName, xenroll/ICEnroll3::get_ContainerName, xenroll/ICEnroll3::put_ContainerName, xenroll/ICEnroll4::ContainerName, xenroll/ICEnroll4::get_ContainerName, xenroll/ICEnroll4::put_ContainerName, xenroll/ICEnroll::ContainerName, xenroll/ICEnroll::get_ContainerName, xenroll/ICEnroll::put_ContainerName
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
 - ICEnroll::get_ContainerName
 - xenroll/ICEnroll::get_ContainerName
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
 - ICEnroll4.ContainerName
 - ICEnroll4.get_ContainerName
 - ICEnroll4.put_ContainerName
 - ICEnroll3.ContainerName
 - ICEnroll3.get_ContainerName
 - ICEnroll3.put_ContainerName
 - ICEnroll2.ContainerName
 - ICEnroll2.get_ContainerName
 - ICEnroll2.put_ContainerName
 - ICEnroll.ContainerName
 - ICEnroll.get_ContainerName
 - ICEnroll.put_ContainerName
 - CEnroll.ContainerName
---

# ICEnroll::get_ContainerName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ContainerName</b> property sets or retrieves the  name of the <a href="/windows/desktop/SecGloss/k-gly">key container</a> to use.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The container specified may be an existing container or a new one. It may only be an existing container if the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">UseExistingKeySet</a> property is set, as long as the key set has not been generated yet. For example, if only an <a href="/windows/desktop/SecGloss/e-gly">exchange key</a> set has been generated for a container, it is still possible to perform a certificate enrollment using the signature key set without setting <b>UseExistingKeySet</b>. The <i>exchange key set</i> could be used if <b>UseExistingKeySet</b> is set beforehand.

By default, a new container is selected each time the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> control is run. This ensures that a new key set is generated. If this property is not explicitly set, a generated GUID is used as the container name.


The <b>ContainerName</b> property affects the behavior of the following methods:

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
BSTR     bstrContainerName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the container name
hr = pEnroll->get_ContainerName( &bstrContainerName );
if ( FAILED ( hr ) )
    printf("Failed getting ContainerName - %x\n", hr );
else
    printf( "ContainerName: %ws\n", bstrContainerName );
// free BSTR when done
if ( NULL != bstrContainerName )
    SysFreeString( bstrContainerName );

// set the container name
// bstrMyName previously set to a valid name
hr = pEnroll->put_ContainerName( bstrMyName );
if ( FAILED ( hr ) )
    printf("Failed setting ContainerName - %x\n", hr );
else
    printf( "ContainerName was set to %ws\n", bstrMyName );
```
