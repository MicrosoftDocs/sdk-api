---
UID: NF:xenroll.ICEnroll.put_CAStoreName
title: ICEnroll::put_CAStoreName
author: windows-sdk-content
description: Sets or retrieves the name of the store where all non-&#0034;ROOT&#0034; and non-&#0034;MY&#0034; certificates are kept.
old-location: security\icenroll4_castorename.htm
tech.root: SecCrypto
ms.assetid: 29616175-7195-430e-a85b-99b50e276e7f
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CAStoreName property [Security], CAStoreName property [Security],CEnroll object, CAStoreName property [Security],ICEnroll interface, CAStoreName property [Security],ICEnroll2 interface, CAStoreName property [Security],ICEnroll3 interface, CAStoreName property [Security],ICEnroll4 interface, CEnroll object [Security],CAStoreName property, ICEnroll interface [Security],CAStoreName property, ICEnroll.CAStoreName, ICEnroll.put_CAStoreName, ICEnroll2 interface [Security],CAStoreName property, ICEnroll2.CAStoreName, ICEnroll2::get_CAStoreName, ICEnroll2::put_CAStoreName, ICEnroll3 interface [Security],CAStoreName property, ICEnroll3.CAStoreName, ICEnroll3::get_CAStoreName, ICEnroll3::put_CAStoreName, ICEnroll4 interface [Security],CAStoreName property, ICEnroll4.CAStoreName, ICEnroll4::CAStoreName, ICEnroll4::get_CAStoreName, ICEnroll4::put_CAStoreName, ICEnroll::get_CAStoreName, ICEnroll::put_CAStoreName, put_CAStoreName, security.icenroll4_castorename, xenroll/ICEnroll2::CAStoreName, xenroll/ICEnroll2::get_CAStoreName, xenroll/ICEnroll2::put_CAStoreName, xenroll/ICEnroll3::CAStoreName, xenroll/ICEnroll3::get_CAStoreName, xenroll/ICEnroll3::put_CAStoreName, xenroll/ICEnroll4::CAStoreName, xenroll/ICEnroll4::get_CAStoreName, xenroll/ICEnroll4::put_CAStoreName, xenroll/ICEnroll::CAStoreName, xenroll/ICEnroll::get_CAStoreName, xenroll/ICEnroll::put_CAStoreName
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
 - ICEnroll4.CAStoreName
 - ICEnroll4.get_CAStoreName
 - ICEnroll4.put_CAStoreName
 - ICEnroll3.CAStoreName
 - ICEnroll3.get_CAStoreName
 - ICEnroll3.put_CAStoreName
 - ICEnroll2.CAStoreName
 - ICEnroll2.get_CAStoreName
 - ICEnroll2.put_CAStoreName
 - ICEnroll.CAStoreName
 - ICEnroll.get_CAStoreName
 - ICEnroll.put_CAStoreName
 - CEnroll.CAStoreName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_CAStoreName


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CAStoreName</b> property sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.

The default value for this property is "CA". This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>CAStoreName</b> property affects the behavior of the following methods:

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
hr = pEnroll-&gt;get_CAStoreName( &amp;bstrStoreName );
if ( FAILED ( hr ) )
    printf("Failed getting CAStoreName - %x\n", hr );
else
    printf( "CAStoreName: %ws\n", bstrStoreName );
// free BSTR when done
if ( NULL != bstrStoreName )
    SysFreeString( bstrStoreName );

// set the storename
// bstrNewName previously set to a valid store name
hr = pEnroll-&gt;put_CAStoreName( bstrNewName );
if ( FAILED ( hr ) )
    printf("Failed setting CAStoreName - %x\n", hr );
else
    printf( "CAStoreName was set to : %ws\n", bstrNewName );</pre>
</td>
</tr>
</table></span></div>


