---
UID: NF:xenroll.ICEnroll.put_RequestStoreType
title: ICEnroll::put_RequestStoreType
author: windows-sdk-content
description: Sets or retrieves the type of store to use for the store specified by the RequestStoreName property. This store type is passed directly to the CertOpenStore function.
old-location: security\icenroll4_requeststoretype.htm
tech.root: seccrypto
ms.assetid: cc0d09bc-3589-454d-a1fe-141af46bc45b
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CEnroll object [Security],RequestStoreType property, ICEnroll interface [Security],RequestStoreType property, ICEnroll.RequestStoreType, ICEnroll.put_RequestStoreType, ICEnroll2 interface [Security],RequestStoreType property, ICEnroll2.RequestStoreType, ICEnroll2::get_RequestStoreType, ICEnroll2::put_RequestStoreType, ICEnroll3 interface [Security],RequestStoreType property, ICEnroll3.RequestStoreType, ICEnroll3::get_RequestStoreType, ICEnroll3::put_RequestStoreType, ICEnroll4 interface [Security],RequestStoreType property, ICEnroll4.RequestStoreType, ICEnroll4::RequestStoreType, ICEnroll4::get_RequestStoreType, ICEnroll4::put_RequestStoreType, ICEnroll::get_RequestStoreType, ICEnroll::put_RequestStoreType, RequestStoreType property [Security], RequestStoreType property [Security],CEnroll object, RequestStoreType property [Security],ICEnroll interface, RequestStoreType property [Security],ICEnroll2 interface, RequestStoreType property [Security],ICEnroll3 interface, RequestStoreType property [Security],ICEnroll4 interface, put_RequestStoreType, security.icenroll4_requeststoretype, sz_CERT_STORE_PROV_SYSTEM, sz_CERT_STORE_PROV_SYSTEM_W, xenroll/ICEnroll2::RequestStoreType, xenroll/ICEnroll2::get_RequestStoreType, xenroll/ICEnroll2::put_RequestStoreType, xenroll/ICEnroll3::RequestStoreType, xenroll/ICEnroll3::get_RequestStoreType, xenroll/ICEnroll3::put_RequestStoreType, xenroll/ICEnroll4::RequestStoreType, xenroll/ICEnroll4::get_RequestStoreType, xenroll/ICEnroll4::put_RequestStoreType, xenroll/ICEnroll::RequestStoreType, xenroll/ICEnroll::get_RequestStoreType, xenroll/ICEnroll::put_RequestStoreType
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
 - ICEnroll4.RequestStoreType
 - ICEnroll4.get_RequestStoreType
 - ICEnroll4.put_RequestStoreType
 - ICEnroll3.RequestStoreType
 - ICEnroll3.get_RequestStoreType
 - ICEnroll3.put_RequestStoreType
 - ICEnroll2.RequestStoreType
 - ICEnroll2.get_RequestStoreType
 - ICEnroll2.put_RequestStoreType
 - ICEnroll.RequestStoreType
 - ICEnroll.get_RequestStoreType
 - ICEnroll.put_RequestStoreType
 - CEnroll.RequestStoreType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_RequestStoreType


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>RequestStoreType</b> property sets or retrieves the type of store to use for the store specified by the 
<a href="https://msdn.microsoft.com/c42d1dc8-ee1c-4bb7-b54f-6ede3301ce03">RequestStoreName</a> property. This store type is passed directly  to the <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> function.

The default value of  this property is sz_CERT_STORE_PROV_SYSTEM. If the default is not to be used, this property must be set to the same value before calls to 
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>/<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a> and again before calls to 
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>/<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>.

Only system stores are supported. This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



Typically, modification of the <b>RequestStoreType</b> property is  performed only in advanced applications.


<b>RequestStoreType</b> affects the behavior of the following methods:

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
hr = pEnroll-&gt;get_RequestStoreType( &amp;bstrStoreType );
if ( FAILED ( hr ) )
    printf("Failed getting RequestStoreType - %x\n", hr );
else
    printf( "RequestStoreType: %ws\n", bstrStoreType );
// free BSTR when done
if ( NULL != bstrStoreType )
    SysFreeString( bstrStoreType );

// set the storetype
// bstrNewType is a BSTR that is previously set to a valid store type
hr = pEnroll-&gt;put_RequestStoreType( bstrNewType );
if ( FAILED ( hr ) )
    printf("Failed setting RequestStoreType - %x\n", hr );
else
    printf( "RequestStoreType was set to %ws\n", bstrNewType );</pre>
</td>
</tr>
</table></span></div>


