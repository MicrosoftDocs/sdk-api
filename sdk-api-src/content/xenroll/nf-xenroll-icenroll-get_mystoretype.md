---
UID: NF:xenroll.ICEnroll.get_MyStoreType
title: ICEnroll::get_MyStoreType
author: windows-sdk-content
description: Sets or retrieves the type of store specified by the MyStoreName property.
old-location: security\icenroll4_mystoretype.htm
tech.root: seccrypto
ms.assetid: 948a9012-b2ac-4bf0-8cae-690ea3ecdb2e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CEnroll object [Security],MyStoreType property, ICEnroll interface [Security],MyStoreType property, ICEnroll.MyStoreType, ICEnroll.get_MyStoreType, ICEnroll2 interface [Security],MyStoreType property, ICEnroll2.MyStoreType, ICEnroll2::get_MyStoreType, ICEnroll2::put_MyStoreType, ICEnroll3 interface [Security],MyStoreType property, ICEnroll3.MyStoreType, ICEnroll3::get_MyStoreType, ICEnroll3::put_MyStoreType, ICEnroll4 interface [Security],MyStoreType property, ICEnroll4.MyStoreType, ICEnroll4::MyStoreType, ICEnroll4::get_MyStoreType, ICEnroll4::put_MyStoreType, ICEnroll::get_MyStoreType, ICEnroll::put_MyStoreType, MyStoreType property [Security], MyStoreType property [Security],CEnroll object, MyStoreType property [Security],ICEnroll interface, MyStoreType property [Security],ICEnroll2 interface, MyStoreType property [Security],ICEnroll3 interface, MyStoreType property [Security],ICEnroll4 interface, get_MyStoreType, security.icenroll4_mystoretype, sz_CERT_STORE_PROV_SYSTEM, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/ICEnroll2::MyStoreType, xenroll/ICEnroll2::get_MyStoreType, xenroll/ICEnroll2::put_MyStoreType, xenroll/ICEnroll3::MyStoreType, xenroll/ICEnroll3::get_MyStoreType, xenroll/ICEnroll3::put_MyStoreType, xenroll/ICEnroll4::MyStoreType, xenroll/ICEnroll4::get_MyStoreType, xenroll/ICEnroll4::put_MyStoreType, xenroll/ICEnroll::MyStoreType, xenroll/ICEnroll::get_MyStoreType, xenroll/ICEnroll::put_MyStoreType
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
 - ICEnroll4.MyStoreType
 - ICEnroll4.get_MyStoreType
 - ICEnroll4.put_MyStoreType
 - ICEnroll3.MyStoreType
 - ICEnroll3.get_MyStoreType
 - ICEnroll3.put_MyStoreType
 - ICEnroll2.MyStoreType
 - ICEnroll2.get_MyStoreType
 - ICEnroll2.put_MyStoreType
 - ICEnroll.MyStoreType
 - ICEnroll.get_MyStoreType
 - ICEnroll.put_MyStoreType
 - CEnroll.MyStoreType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::get_MyStoreType


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreType</b> property sets or retrieves the type of store  specified by the 
<a href="https://msdn.microsoft.com/aa08e88d-bd1f-4bd6-806e-56f720846623">MyStoreName</a> property.   This store type is passed directly on to <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>.

The default value for this property is sz_CERT_STORE_PROV_SYSTEM. Only system stores are supported. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>MyStoreType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>
</li>
</ul>


The ability to set this property is disabled when  the Certificate Enrollment Control is executed as a scripted control.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR     bstrStoreType = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storetype
hr = pEnroll-&gt;get_MyStoreType( &amp;bstrStoreType );
if ( FAILED ( hr ) )
    printf("Failed getting MyStoreType - %x\n", hr );
else
    printf( "MyStoreType: %ws\n", bstrStoreType );
// free BSTR when done
if ( NULL != bstrStoreType )
    SysFreeString( bstrStoreType );

// set the storetype
// bstrNewType previously set to a valid store type
hr = pEnroll-&gt;put_MyStoreType( bstrNewType );
if ( FAILED ( hr ) )
    printf("Failed setting MyStoreType - %x\n", hr );
else
    printf( "MyStoreType was set to %ws\n", bstrNewType );</pre>
</td>
</tr>
</table></span></div>


