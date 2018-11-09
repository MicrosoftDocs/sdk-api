---
UID: NF:xenroll.ICEnroll.get_MyStoreFlags
title: ICEnroll::get_MyStoreFlags
author: windows-sdk-content
description: Sets or retrieves the registry location used for MY store.
old-location: security\icenroll4_mystoreflags.htm
tech.root: seccrypto
ms.assetid: 0616c666-9cfc-48f9-93a2-91d51d8dff04
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CEnroll object [Security],MyStoreFlags property, ICEnroll interface [Security],MyStoreFlags property, ICEnroll.MyStoreFlags, ICEnroll.get_MyStoreFlags, ICEnroll2 interface [Security],MyStoreFlags property, ICEnroll2.MyStoreFlags, ICEnroll2::get_MyStoreFlags, ICEnroll2::put_MyStoreFlags, ICEnroll3 interface [Security],MyStoreFlags property, ICEnroll3.MyStoreFlags, ICEnroll3::get_MyStoreFlags, ICEnroll3::put_MyStoreFlags, ICEnroll4 interface [Security],MyStoreFlags property, ICEnroll4.MyStoreFlags, ICEnroll4::MyStoreFlags, ICEnroll4::get_MyStoreFlags, ICEnroll4::put_MyStoreFlags, ICEnroll::get_MyStoreFlags, ICEnroll::put_MyStoreFlags, MyStoreFlags property [Security], MyStoreFlags property [Security],CEnroll object, MyStoreFlags property [Security],ICEnroll interface, MyStoreFlags property [Security],ICEnroll2 interface, MyStoreFlags property [Security],ICEnroll3 interface, MyStoreFlags property [Security],ICEnroll4 interface, get_MyStoreFlags, security.icenroll4_mystoreflags, xenroll/ICEnroll2::MyStoreFlags, xenroll/ICEnroll2::get_MyStoreFlags, xenroll/ICEnroll2::put_MyStoreFlags, xenroll/ICEnroll3::MyStoreFlags, xenroll/ICEnroll3::get_MyStoreFlags, xenroll/ICEnroll3::put_MyStoreFlags, xenroll/ICEnroll4::MyStoreFlags, xenroll/ICEnroll4::get_MyStoreFlags, xenroll/ICEnroll4::put_MyStoreFlags, xenroll/ICEnroll::MyStoreFlags, xenroll/ICEnroll::get_MyStoreFlags, xenroll/ICEnroll::put_MyStoreFlags
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
 - ICEnroll4.MyStoreFlags
 - ICEnroll4.get_MyStoreFlags
 - ICEnroll4.put_MyStoreFlags
 - ICEnroll3.MyStoreFlags
 - ICEnroll3.get_MyStoreFlags
 - ICEnroll3.put_MyStoreFlags
 - ICEnroll2.MyStoreFlags
 - ICEnroll2.get_MyStoreFlags
 - ICEnroll2.put_MyStoreFlags
 - ICEnroll.MyStoreFlags
 - ICEnroll.get_MyStoreFlags
 - ICEnroll.put_MyStoreFlags
 - CEnroll.MyStoreFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::get_MyStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreFlags</b> property sets or retrieves the registry location used for MY store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>MyStoreFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> CryptoAPI function by using its <i>dwFlags</i> parameter.


The <b>MyStoreFlags</b> property should be set before using the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>
</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD    dwFlags;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// retrieve the flag value
hr = pEnroll-&gt;get_MyStoreFlags( &amp;dwFlags );
if ( FAILED ( hr ) )
    printf("Failed retrieving MyStoreFlags - %x\n", hr );
else
    printf("MyStoreFlags is %x\n", dwFlags );

// set the flag
hr = pEnroll-&gt;put_MyStoreFlags( CERT_SYSTEM_STORE_LOCAL_MACHINE );
if ( FAILED ( hr ) )
    printf("Failed updating MyStoreFlags - %x\n", hr );
else
    printf("Updated MyStoreFlags\n");</pre>
</td>
</tr>
</table></span></div>


