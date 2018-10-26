---
UID: NF:xenroll.ICEnroll.put_GenKeyFlags
title: ICEnroll::put_GenKeyFlags
author: windows-sdk-content
description: Sets or retrieves the values passed to the CryptGenKey function when the certificate request is generated.
old-location: security\icenroll4_genkeyflags.htm
tech.root: seccrypto
ms.assetid: d22fe4d4-a939-4f77-8e11-f9312c81ec1e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CEnroll object [Security],GenKeyFlags property, GenKeyFlags property [Security], GenKeyFlags property [Security],CEnroll object, GenKeyFlags property [Security],ICEnroll interface, GenKeyFlags property [Security],ICEnroll2 interface, GenKeyFlags property [Security],ICEnroll3 interface, GenKeyFlags property [Security],ICEnroll4 interface, ICEnroll interface [Security],GenKeyFlags property, ICEnroll.GenKeyFlags, ICEnroll.put_GenKeyFlags, ICEnroll2 interface [Security],GenKeyFlags property, ICEnroll2.GenKeyFlags, ICEnroll2::get_GenKeyFlags, ICEnroll2::put_GenKeyFlags, ICEnroll3 interface [Security],GenKeyFlags property, ICEnroll3.GenKeyFlags, ICEnroll3::get_GenKeyFlags, ICEnroll3::put_GenKeyFlags, ICEnroll4 interface [Security],GenKeyFlags property, ICEnroll4.GenKeyFlags, ICEnroll4::GenKeyFlags, ICEnroll4::get_GenKeyFlags, ICEnroll4::put_GenKeyFlags, ICEnroll::get_GenKeyFlags, ICEnroll::put_GenKeyFlags, put_GenKeyFlags, security.icenroll4_genkeyflags, xenroll/ICEnroll2::GenKeyFlags, xenroll/ICEnroll2::get_GenKeyFlags, xenroll/ICEnroll2::put_GenKeyFlags, xenroll/ICEnroll3::GenKeyFlags, xenroll/ICEnroll3::get_GenKeyFlags, xenroll/ICEnroll3::put_GenKeyFlags, xenroll/ICEnroll4::GenKeyFlags, xenroll/ICEnroll4::get_GenKeyFlags, xenroll/ICEnroll4::put_GenKeyFlags, xenroll/ICEnroll::GenKeyFlags, xenroll/ICEnroll::get_GenKeyFlags, xenroll/ICEnroll::put_GenKeyFlags
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
 - ICEnroll4.GenKeyFlags
 - ICEnroll4.get_GenKeyFlags
 - ICEnroll4.put_GenKeyFlags
 - ICEnroll3.GenKeyFlags
 - ICEnroll3.get_GenKeyFlags
 - ICEnroll3.put_GenKeyFlags
 - ICEnroll2.GenKeyFlags
 - ICEnroll2.get_GenKeyFlags
 - ICEnroll2.put_GenKeyFlags
 - ICEnroll.GenKeyFlags
 - ICEnroll.get_GenKeyFlags
 - ICEnroll.put_GenKeyFlags
 - CEnroll.GenKeyFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_GenKeyFlags


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GenKeyFlags</b> property sets or retrieves the values passed to the  <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>  function when the certificate request is generated.

By default, the <b>GenKeyFlags</b> property is set to zero. However, when a .pvk file is specified, the value of <b>GenKeyFlags</b> defaults to CRYPT_EXPORTABLE. For more information, see Remarks.

This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



By default, private keys are not exportable unless a .pvk file is requested. To make the private key exportable without specifying a .pvk file, set <b>GenKeyFlags</b> to CRYPT_EXPORTABLE.

To specify a .pvk file name,  use the 
<a href="https://msdn.microsoft.com/3f841bb2-6cfd-4712-bb71-5c3d9d462fab">PVKFileName</a> property.

The <b>GenKeyFlags</b> property value is passed to the 
<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> CryptoAPI function by using its <i>dwFlags</i> parameter.

If the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>  (CSP) does not support exportable private keys, an error occurs.


The <b>GenKeyFlags</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2a1c1c4-dbbf-423c-bf59-da0ab9a71078">createRequest</a>
</li>
</ul>


<div class="alert"><b>Note</b>  The default value for the <b>GenKeyFlags</b> property is zero. If you need to change this value, you must do so before calling these methods. After calling any of these methods, you cannot change the <b>GenKeyFlags</b> property value.</div>
<div> </div>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LONG     lGenKey;
HRESULT  hr;

// pEnroll is a previously instantiated ICEnroll interface pointer.

// Get the GenKeyFlags value.
hr = pEnroll-&gt;get_GenKeyFlags( &amp;lGenKey );
if (FAILED( hr ))
    printf("Failed get_GenKeyFlags - %x\n", hr );
else
    printf( "GenKeyFlags: %d\n", lGenKey );

// Set the GenKeyFlags value.
hr = pEnroll-&gt;put_GenKeyFlags( CRYPT_EXPORTABLE );
if (FAILED( hr ))
    printf("Failed put_GenKeyFlags - %x\n", hr );
else
    printf( "GenKeyFlags set to %d\n", CRYPT_EXPORTABLE );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>



<a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a>



<a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

