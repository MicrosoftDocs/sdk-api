---
UID: NF:xenroll.ICEnroll.put_UseExistingKeySet
title: ICEnroll::put_UseExistingKeySet
author: windows-sdk-content
description: Sets or retrieves a Boolean value that determines whether the existing keys should be used.
old-location: security\icenroll4_useexistingkeyset.htm
tech.root: seccrypto
ms.assetid: e5115033-bda1-4160-84b3-80c692bf64fb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CEnroll object [Security],UseExistingKeySet property, ICEnroll interface [Security],UseExistingKeySet property, ICEnroll.UseExistingKeySet, ICEnroll.put_UseExistingKeySet, ICEnroll2 interface [Security],UseExistingKeySet property, ICEnroll2.UseExistingKeySet, ICEnroll2::get_UseExistingKeySet, ICEnroll2::put_UseExistingKeySet, ICEnroll3 interface [Security],UseExistingKeySet property, ICEnroll3.UseExistingKeySet, ICEnroll3::get_UseExistingKeySet, ICEnroll3::put_UseExistingKeySet, ICEnroll4 interface [Security],UseExistingKeySet property, ICEnroll4.UseExistingKeySet, ICEnroll4::UseExistingKeySet, ICEnroll4::get_UseExistingKeySet, ICEnroll4::put_UseExistingKeySet, ICEnroll::get_UseExistingKeySet, ICEnroll::put_UseExistingKeySet, UseExistingKeySet property [Security], UseExistingKeySet property [Security],CEnroll object, UseExistingKeySet property [Security],ICEnroll interface, UseExistingKeySet property [Security],ICEnroll2 interface, UseExistingKeySet property [Security],ICEnroll3 interface, UseExistingKeySet property [Security],ICEnroll4 interface, put_UseExistingKeySet, security.icenroll4_useexistingkeyset, xenroll/ICEnroll2::UseExistingKeySet, xenroll/ICEnroll2::get_UseExistingKeySet, xenroll/ICEnroll2::put_UseExistingKeySet, xenroll/ICEnroll3::UseExistingKeySet, xenroll/ICEnroll3::get_UseExistingKeySet, xenroll/ICEnroll3::put_UseExistingKeySet, xenroll/ICEnroll4::UseExistingKeySet, xenroll/ICEnroll4::get_UseExistingKeySet, xenroll/ICEnroll4::put_UseExistingKeySet, xenroll/ICEnroll::UseExistingKeySet, xenroll/ICEnroll::get_UseExistingKeySet, xenroll/ICEnroll::put_UseExistingKeySet
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
 - ICEnroll4.UseExistingKeySet
 - ICEnroll4.get_UseExistingKeySet
 - ICEnroll4.put_UseExistingKeySet
 - ICEnroll3.UseExistingKeySet
 - ICEnroll3.get_UseExistingKeySet
 - ICEnroll3.put_UseExistingKeySet
 - ICEnroll2.UseExistingKeySet
 - ICEnroll2.get_UseExistingKeySet
 - ICEnroll2.put_UseExistingKeySet
 - ICEnroll.UseExistingKeySet
 - ICEnroll.get_UseExistingKeySet
 - ICEnroll.put_UseExistingKeySet
 - CEnroll.UseExistingKeySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_UseExistingKeySet


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>UseExistingKeySet</b> property sets or retrieves a Boolean value that determines whether the existing keys should be used.

This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



 If an existing key set is used, the <b>UseExistingKeySet</b> property must be set to true.


The <b>UseExistingKeySet</b> property affects the behavior of the following methods:

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
<pre>BOOL     bUEKS;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the UseExistingKeySet value
hr = pEnroll-&gt;get_UseExistingKeySet( &amp;bUEKS );
if (FAILED( hr ))
    printf("Failed get_UseExistingKeySet - %x\n", hr );
else
    printf( "UseExistingKeySet: %d\n", bUEKS );

// set the UseExistingKeySet value
hr = pEnroll-&gt;put_UseExistingKeySet( TRUE );
if (FAILED( hr ))
    printf("Failed put_UseExistingKeySet - %x\n", hr );
else
    printf( "UseExistingKeySet set to TRUE\n" );</pre>
</td>
</tr>
</table></span></div>


