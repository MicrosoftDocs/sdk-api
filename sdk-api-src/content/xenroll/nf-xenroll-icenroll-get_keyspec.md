---
UID: NF:xenroll.ICEnroll.get_KeySpec
title: ICEnroll::get_KeySpec
author: windows-sdk-content
description: The KeySpec property of ICEnroll4 sets or retrieves the type of key generated.
old-location: security\icenroll4_keyspec.htm
tech.root: seccrypto
ms.assetid: 30cc7c86-29ce-42e9-b9dc-d29f5b5450a5
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CEnroll object [Security],KeySpec property, ICEnroll interface [Security],KeySpec property, ICEnroll.KeySpec, ICEnroll.get_KeySpec, ICEnroll2 interface [Security],KeySpec property, ICEnroll2.KeySpec, ICEnroll2::get_KeySpec, ICEnroll2::put_KeySpec, ICEnroll3 interface [Security],KeySpec property, ICEnroll3.KeySpec, ICEnroll3::get_KeySpec, ICEnroll3::put_KeySpec, ICEnroll4 interface [Security],KeySpec property, ICEnroll4.KeySpec, ICEnroll4::KeySpec, ICEnroll4::get_KeySpec, ICEnroll4::put_KeySpec, ICEnroll::get_KeySpec, ICEnroll::put_KeySpec, KeySpec property [Security], KeySpec property [Security],CEnroll object, KeySpec property [Security],ICEnroll interface, KeySpec property [Security],ICEnroll2 interface, KeySpec property [Security],ICEnroll3 interface, KeySpec property [Security],ICEnroll4 interface, get_KeySpec, security.icenroll4_keyspec, xenroll/ICEnroll2::KeySpec, xenroll/ICEnroll2::get_KeySpec, xenroll/ICEnroll2::put_KeySpec, xenroll/ICEnroll3::KeySpec, xenroll/ICEnroll3::get_KeySpec, xenroll/ICEnroll3::put_KeySpec, xenroll/ICEnroll4::KeySpec, xenroll/ICEnroll4::get_KeySpec, xenroll/ICEnroll4::put_KeySpec, xenroll/ICEnroll::KeySpec, xenroll/ICEnroll::get_KeySpec, xenroll/ICEnroll::put_KeySpec
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
 - ICEnroll4.KeySpec
 - ICEnroll4.get_KeySpec
 - ICEnroll4.put_KeySpec
 - ICEnroll3.KeySpec
 - ICEnroll3.get_KeySpec
 - ICEnroll3.put_KeySpec
 - ICEnroll2.KeySpec
 - ICEnroll2.get_KeySpec
 - ICEnroll2.put_KeySpec
 - ICEnroll.KeySpec
 - ICEnroll.get_KeySpec
 - ICEnroll.put_KeySpec
 - CEnroll.KeySpec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::get_KeySpec


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>KeySpec</b> property sets or retrieves the  type of key generated.

 Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For the Microsoft Base Cryptographic Provider, the <b>KeySpec</b> property has a value of AT_KEYEXCHANGE for <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>, or AT_SIGNATURE for signature keys. The default is AT_SIGNATURE.

For information about the other Microsoft CSPs, see 
<a href="https://msdn.microsoft.com/4e6eb2df-a917-4533-b9f1-8da39598d0b8">Cryptographic Service Providers</a> in the CryptoAPI 2.0 documentation.

For information about other CSPs, see the documentation provided with the CSP.


The <b>KeySpec</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD    dwKeySpec;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the KeySpec value
hr = pEnroll-&gt;get_KeySpec( &amp;dwKeySpec );
if (FAILED( hr ))
    printf("Failed get_KeySpec - %x\n", hr );
else
    printf( "KeySpec: %d\n", dwKeySpec );

// set the KeySpec value
hr = pEnroll-&gt;put_KeySpec( AT_KEYEXCHANGE );
if (FAILED( hr ))
    printf("Failed put_KeySpec - %x\n", hr );
else
    printf( "KeySpec set to %d\n", AT_KEYEXCHANGE );</pre>
</td>
</tr>
</table></span></div>


