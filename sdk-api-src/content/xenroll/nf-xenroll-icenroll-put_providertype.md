---
UID: NF:xenroll.ICEnroll.put_ProviderType
title: ICEnroll::put_ProviderType
author: windows-sdk-content
description: The ProviderType property of ICEnroll4 sets or retrieves the type of provider.
old-location: security\icenroll4_providertype.htm
tech.root: seccrypto
ms.assetid: 90daa97a-350e-4307-80a5-b018cc1f0e86
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CEnroll object [Security],ProviderType property, ICEnroll interface [Security],ProviderType property, ICEnroll.ProviderType, ICEnroll.put_ProviderType, ICEnroll2 interface [Security],ProviderType property, ICEnroll2.ProviderType, ICEnroll2::get_ProviderType, ICEnroll2::put_ProviderType, ICEnroll3 interface [Security],ProviderType property, ICEnroll3.ProviderType, ICEnroll3::get_ProviderType, ICEnroll3::put_ProviderType, ICEnroll4 interface [Security],ProviderType property, ICEnroll4.ProviderType, ICEnroll4::ProviderType, ICEnroll4::get_ProviderType, ICEnroll4::put_ProviderType, ICEnroll::get_ProviderType, ICEnroll::put_ProviderType, ProviderType property [Security], ProviderType property [Security],CEnroll object, ProviderType property [Security],ICEnroll interface, ProviderType property [Security],ICEnroll2 interface, ProviderType property [Security],ICEnroll3 interface, ProviderType property [Security],ICEnroll4 interface, put_ProviderType, security.icenroll4_providertype, xenroll/ICEnroll2::ProviderType, xenroll/ICEnroll2::get_ProviderType, xenroll/ICEnroll2::put_ProviderType, xenroll/ICEnroll3::ProviderType, xenroll/ICEnroll3::get_ProviderType, xenroll/ICEnroll3::put_ProviderType, xenroll/ICEnroll4::ProviderType, xenroll/ICEnroll4::get_ProviderType, xenroll/ICEnroll4::put_ProviderType, xenroll/ICEnroll::ProviderType, xenroll/ICEnroll::get_ProviderType, xenroll/ICEnroll::put_ProviderType
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
 - ICEnroll4.ProviderType
 - ICEnroll4.get_ProviderType
 - ICEnroll4.put_ProviderType
 - ICEnroll3.ProviderType
 - ICEnroll3.get_ProviderType
 - ICEnroll3.put_ProviderType
 - ICEnroll2.ProviderType
 - ICEnroll2.get_ProviderType
 - ICEnroll2.put_ProviderType
 - ICEnroll.ProviderType
 - ICEnroll.get_ProviderType
 - ICEnroll.put_ProviderType
 - CEnroll.ProviderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_ProviderType


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderType</b> property sets or retrieves the type of provider.

The value of the <b>ProviderType</b> property is passed to the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use. The default value for this property is 1. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For general information about provider types, see 
<a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>.

For more information about valid values for the Microsoft Base Cryptographic Provider, see the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function.

For provider type information for other CSPs, see the documentation provided with the CSP.

The <b>ProviderType</b> property value is passed to <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>  by using its <i>dwProvType</i> parameter.


The <b>ProviderType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05188aee-2b03-46bc-89f4-506a019496a4">enumProviders</a>
</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD    dwProvType;
HRESULT  hr;

// Get the ProviderType value.
// pEnroll is previously instantiated ICEnroll interface pointer
hr = pEnroll-&gt;get_ProviderType(&amp;dwProvType);
if (FAILED( hr ))
    printf("Failed get_ProviderType - %x\n", hr);
else
    printf("ProviderType: %d\n", dwProvType);

// Set the ProviderType value.
hr = pEnroll-&gt;put_ProviderType(PROV_MS_EXCHANGE);
if (FAILED(hr))
    printf("Failed put_ProviderType - %x\n", hr);
else
    printf("ProviderType set to %d\n", PROV_MS_EXCHANGE);</pre>
</td>
</tr>
</table></span></div>


