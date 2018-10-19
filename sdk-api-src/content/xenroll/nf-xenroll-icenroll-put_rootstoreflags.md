---
UID: NF:xenroll.ICEnroll.put_RootStoreFlags
title: ICEnroll::put_RootStoreFlags
author: windows-sdk-content
description: The RootStoreFlags property of ICEnroll4 sets or retrieves the registry location used for the root store.
old-location: security\icenroll4_rootstoreflags.htm
tech.root: seccrypto
ms.assetid: bf844047-4f5a-42de-a446-195371c0dbcf
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CEnroll object [Security],RootStoreFlags property, ICEnroll interface [Security],RootStoreFlags property, ICEnroll.RootStoreFlags, ICEnroll.put_RootStoreFlags, ICEnroll2 interface [Security],RootStoreFlags property, ICEnroll2.RootStoreFlags, ICEnroll2::get_RootStoreFlags, ICEnroll2::put_RootStoreFlags, ICEnroll3 interface [Security],RootStoreFlags property, ICEnroll3.RootStoreFlags, ICEnroll3::get_RootStoreFlags, ICEnroll3::put_RootStoreFlags, ICEnroll4 interface [Security],RootStoreFlags property, ICEnroll4.RootStoreFlags, ICEnroll4::RootStoreFlags, ICEnroll4::get_RootStoreFlags, ICEnroll4::put_RootStoreFlags, ICEnroll::get_RootStoreFlags, ICEnroll::put_RootStoreFlags, RootStoreFlags property [Security], RootStoreFlags property [Security],CEnroll object, RootStoreFlags property [Security],ICEnroll interface, RootStoreFlags property [Security],ICEnroll2 interface, RootStoreFlags property [Security],ICEnroll3 interface, RootStoreFlags property [Security],ICEnroll4 interface, put_RootStoreFlags, security.icenroll4_rootstoreflags, xenroll/ICEnroll2::RootStoreFlags, xenroll/ICEnroll2::get_RootStoreFlags, xenroll/ICEnroll2::put_RootStoreFlags, xenroll/ICEnroll3::RootStoreFlags, xenroll/ICEnroll3::get_RootStoreFlags, xenroll/ICEnroll3::put_RootStoreFlags, xenroll/ICEnroll4::RootStoreFlags, xenroll/ICEnroll4::get_RootStoreFlags, xenroll/ICEnroll4::put_RootStoreFlags, xenroll/ICEnroll::RootStoreFlags, xenroll/ICEnroll::get_RootStoreFlags, xenroll/ICEnroll::put_RootStoreFlags
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
 - ICEnroll4.RootStoreFlags
 - ICEnroll4.get_RootStoreFlags
 - ICEnroll4.put_RootStoreFlags
 - ICEnroll3.RootStoreFlags
 - ICEnroll3.get_RootStoreFlags
 - ICEnroll3.put_RootStoreFlags
 - ICEnroll2.RootStoreFlags
 - ICEnroll2.get_RootStoreFlags
 - ICEnroll2.put_RootStoreFlags
 - ICEnroll.RootStoreFlags
 - ICEnroll.get_RootStoreFlags
 - ICEnroll.put_RootStoreFlags
 - CEnroll.RootStoreFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_RootStoreFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RootStoreFlags</b> property sets or retrieves the registry location used for the root store.

The default value for  this property  is CERT_SYSTEM_STORE_CURRENT_USER. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>RootStoreFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> CryptoAPI function by using  its <i>dwFlags</i> parameter.


The <b>RootStoreFlags</b> property should be set before using the following methods:

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

// pEnroll is previously instantiated ICEnroll interface pointer.

// Retrieve the flag value.
hr = pEnroll-&gt;get_RootStoreFlags( &amp;dwFlags );
if ( FAILED ( hr ) )
    printf("Failed retrieving RootStoreFlags - %x\n", hr );
else
    printf("RootStoreFlags is %x\n", dwFlags );

// Set the flag.
hr = pEnroll-&gt;put_RootStoreFlags( CERT_SYSTEM_STORE_LOCAL_MACHINE );
if ( FAILED ( hr ) )
    printf("Failed updating RootStoreFlags - %x\n", hr );
else
    printf("Updated RootStoreFlags\n");</pre>
</td>
</tr>
</table></span></div>


