---
UID: NF:xenroll.ICEnroll.put_ProviderFlags
title: ICEnroll::put_ProviderFlags (xenroll.h)
author: windows-sdk-content
description: Sets or retrieves the provider type.
old-location: security\icenroll4_providerflags.htm
tech.root: SecCrypto
ms.assetid: ddf92921-368f-4769-b2c1-b9d6a94b0fcb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CEnroll object [Security],ProviderFlags property, ICEnroll interface [Security],ProviderFlags property, ICEnroll.ProviderFlags, ICEnroll.put_ProviderFlags, ICEnroll2 interface [Security],ProviderFlags property, ICEnroll2.ProviderFlags, ICEnroll2::get_ProviderFlags, ICEnroll2::put_ProviderFlags, ICEnroll3 interface [Security],ProviderFlags property, ICEnroll3.ProviderFlags, ICEnroll3::get_ProviderFlags, ICEnroll3::put_ProviderFlags, ICEnroll4 interface [Security],ProviderFlags property, ICEnroll4.ProviderFlags, ICEnroll4::ProviderFlags, ICEnroll4::get_ProviderFlags, ICEnroll4::put_ProviderFlags, ICEnroll::get_ProviderFlags, ICEnroll::put_ProviderFlags, ProviderFlags property [Security], ProviderFlags property [Security],CEnroll object, ProviderFlags property [Security],ICEnroll interface, ProviderFlags property [Security],ICEnroll2 interface, ProviderFlags property [Security],ICEnroll3 interface, ProviderFlags property [Security],ICEnroll4 interface, put_ProviderFlags, security.icenroll4_providerflags, xenroll/ICEnroll2::ProviderFlags, xenroll/ICEnroll2::get_ProviderFlags, xenroll/ICEnroll2::put_ProviderFlags, xenroll/ICEnroll3::ProviderFlags, xenroll/ICEnroll3::get_ProviderFlags, xenroll/ICEnroll3::put_ProviderFlags, xenroll/ICEnroll4::ProviderFlags, xenroll/ICEnroll4::get_ProviderFlags, xenroll/ICEnroll4::put_ProviderFlags, xenroll/ICEnroll::ProviderFlags, xenroll/ICEnroll::get_ProviderFlags, xenroll/ICEnroll::put_ProviderFlags
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
 - ICEnroll4.ProviderFlags
 - ICEnroll4.get_ProviderFlags
 - ICEnroll4.put_ProviderFlags
 - ICEnroll3.ProviderFlags
 - ICEnroll3.get_ProviderFlags
 - ICEnroll3.put_ProviderFlags
 - ICEnroll2.ProviderFlags
 - ICEnroll2.get_ProviderFlags
 - ICEnroll2.put_ProviderFlags
 - ICEnroll.ProviderFlags
 - ICEnroll.get_ProviderFlags
 - ICEnroll.put_ProviderFlags
 - CEnroll.ProviderFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_ProviderFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderFlags</b> property sets or retrieves the provider type.

The <b>ProviderFlags</b> property is passed to the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use.

The default value for this property is zero. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For  more information about   valid <b>ProviderFlags</b> values for the Microsoft Base Cryptographic Provider, see the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function.

For information about  other CSPs, see the documentation provided with the CSP.

The <b>ProviderFlags</b> property value is passed to <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>  by using  its <i>dwFlags</i> parameter.


The <b>ProviderFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
</ul>



#### Examples


```cpp
DWORD    dwProvFlags;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer
// get the ProviderFlags value
hr = pEnroll->get_ProviderFlags( &dwProvFlags );
if (FAILED( hr ))
    printf("Failed get_ProviderFlags - %x\n", hr );
else
    printf( "ProviderFlags: %d\n", dwProvFlags );

// Set the ProviderFlags value.
hr = pEnroll->put_ProviderFlags(CRYPT_MACHINE_KEYSET);
if (FAILED( hr ))
    printf("Failed put_ProviderFlags - %x\n", hr );
else
    printf( "ProviderFlags set to %d\n", CRYPT_MACHINE_KEYSET  );
```




