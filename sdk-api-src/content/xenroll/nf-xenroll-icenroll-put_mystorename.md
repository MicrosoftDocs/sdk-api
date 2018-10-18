---
UID: NF:xenroll.ICEnroll.put_MyStoreName
title: ICEnroll::put_MyStoreName
author: windows-sdk-content
description: Sets or retrieves the name of the store where certificates with linked private keys are kept.
old-location: security\icenroll4_mystorename.htm
tech.root: seccrypto
ms.assetid: aa08e88d-bd1f-4bd6-806e-56f720846623
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CEnroll object [Security],MyStoreName property, ICEnroll interface [Security],MyStoreName property, ICEnroll.MyStoreName, ICEnroll.put_MyStoreName, ICEnroll2 interface [Security],MyStoreName property, ICEnroll2.MyStoreName, ICEnroll2::get_MyStoreName, ICEnroll2::put_MyStoreName, ICEnroll3 interface [Security],MyStoreName property, ICEnroll3.MyStoreName, ICEnroll3::get_MyStoreName, ICEnroll3::put_MyStoreName, ICEnroll4 interface [Security],MyStoreName property, ICEnroll4.MyStoreName, ICEnroll4::MyStoreName, ICEnroll4::get_MyStoreName, ICEnroll4::put_MyStoreName, ICEnroll::get_MyStoreName, ICEnroll::put_MyStoreName, MyStoreName property [Security], MyStoreName property [Security],CEnroll object, MyStoreName property [Security],ICEnroll interface, MyStoreName property [Security],ICEnroll2 interface, MyStoreName property [Security],ICEnroll3 interface, MyStoreName property [Security],ICEnroll4 interface, put_MyStoreName, security.icenroll4_mystorename, xenroll/ICEnroll2::MyStoreName, xenroll/ICEnroll2::get_MyStoreName, xenroll/ICEnroll2::put_MyStoreName, xenroll/ICEnroll3::MyStoreName, xenroll/ICEnroll3::get_MyStoreName, xenroll/ICEnroll3::put_MyStoreName, xenroll/ICEnroll4::MyStoreName, xenroll/ICEnroll4::get_MyStoreName, xenroll/ICEnroll4::put_MyStoreName, xenroll/ICEnroll::MyStoreName, xenroll/ICEnroll::get_MyStoreName, xenroll/ICEnroll::put_MyStoreName
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
 - ICEnroll4.MyStoreName
 - ICEnroll4.get_MyStoreName
 - ICEnroll4.put_MyStoreName
 - ICEnroll3.MyStoreName
 - ICEnroll3.get_MyStoreName
 - ICEnroll3.put_MyStoreName
 - ICEnroll2.MyStoreName
 - ICEnroll2.get_MyStoreName
 - ICEnroll2.put_MyStoreName
 - ICEnroll.MyStoreName
 - ICEnroll.get_MyStoreName
 - ICEnroll.put_MyStoreName
 - CEnroll.MyStoreName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_MyStoreName


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>MyStoreName</b> property sets or retrieves the name of the store  where certificates with linked <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a> are kept.

The value of <b>MyStoreName</b> specifies the store in which to place the new certificate produced from 
<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a> or 
<a href="https://msdn.microsoft.com/dae9f6b8-6690-47cc-9397-168c1ff54c55">acceptFilePKCS7</a>. The default value for this property is "MY". This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>MyStoreName</b> property affects the behavior of the following methods:

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
<pre>BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the storename
hr = pEnroll-&gt;get_MyStoreName( &amp;bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting MyStoreName - %x\n", hr );
else
    printf( "MyStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName previously set to a valid store name
hr = pEnroll-&gt;put_MyStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting MyStoreName - %x\n", hr );
else
    printf( "MyStoreName was set to : %ws\n", bstrNewName );</pre>
</td>
</tr>
</table></span></div>


