---
UID: NF:xenroll.ICEnroll.get_WriteCertToCSP
title: ICEnroll::get_WriteCertToCSP
author: windows-driver-content
description: The WriteCertToCSP property of ICEnroll4 sets or retrieves a Boolean value that determines whether a certificate should be written to the cryptographic service provider (CSP).
old-location: security\icenroll4_writecerttocsp.htm
old-project: SecCrypto
ms.assetid: cc622f5b-e6d0-48c5-8535-29d6d4b02129
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CEnroll object [Security],WriteCertToCSP property, ICEnroll interface [Security],WriteCertToCSP property, ICEnroll.WriteCertToCSP, ICEnroll.get_WriteCertToCSP, ICEnroll2 interface [Security],WriteCertToCSP property, ICEnroll2.WriteCertToCSP, ICEnroll2::get_WriteCertToCSP, ICEnroll2::put_WriteCertToCSP, ICEnroll3 interface [Security],WriteCertToCSP property, ICEnroll3.WriteCertToCSP, ICEnroll3::get_WriteCertToCSP, ICEnroll3::put_WriteCertToCSP, ICEnroll4 interface [Security],WriteCertToCSP property, ICEnroll4.WriteCertToCSP, ICEnroll4::WriteCertToCSP, ICEnroll4::get_WriteCertToCSP, ICEnroll4::put_WriteCertToCSP, ICEnroll::get_WriteCertToCSP, ICEnroll::put_WriteCertToCSP, WriteCertToCSP property [Security], WriteCertToCSP property [Security],CEnroll object, WriteCertToCSP property [Security],ICEnroll interface, WriteCertToCSP property [Security],ICEnroll2 interface, WriteCertToCSP property [Security],ICEnroll3 interface, WriteCertToCSP property [Security],ICEnroll4 interface, get_WriteCertToCSP, security.icenroll4_writecerttocsp, xenroll/ICEnroll2::WriteCertToCSP, xenroll/ICEnroll2::get_WriteCertToCSP, xenroll/ICEnroll2::put_WriteCertToCSP, xenroll/ICEnroll3::WriteCertToCSP, xenroll/ICEnroll3::get_WriteCertToCSP, xenroll/ICEnroll3::put_WriteCertToCSP, xenroll/ICEnroll4::WriteCertToCSP, xenroll/ICEnroll4::get_WriteCertToCSP, xenroll/ICEnroll4::put_WriteCertToCSP, xenroll/ICEnroll::WriteCertToCSP, xenroll/ICEnroll::get_WriteCertToCSP, xenroll/ICEnroll::put_WriteCertToCSP
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	ICEnroll4.WriteCertToCSP
-	ICEnroll4.get_WriteCertToCSP
-	ICEnroll4.put_WriteCertToCSP
-	ICEnroll3.WriteCertToCSP
-	ICEnroll3.get_WriteCertToCSP
-	ICEnroll3.put_WriteCertToCSP
-	ICEnroll2.WriteCertToCSP
-	ICEnroll2.get_WriteCertToCSP
-	ICEnroll2.put_WriteCertToCSP
-	ICEnroll.WriteCertToCSP
-	ICEnroll.get_WriteCertToCSP
-	ICEnroll.put_WriteCertToCSP
-	CEnroll.WriteCertToCSP
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll::get_WriteCertToCSP


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToCSP</b> property sets or retrieves a Boolean value that determines whether a certificate should be written to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).

This property was first defined by the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



This property is typically used with smart cards, where the certificate is written to the smart card in addition to being written to the "MY" store.

The default value is <b>true</b>, which means that the Certificate Enrollment Control will try to write the certificate to the CSP but will not fail unless a hardware token error is encountered. If this value is <b>true</b>, but no smart card or other hardware-dependent CSP is installed, then hardware token errors will be ignored.

To explicitly force that the Certificate Enrollment Control not attempt to write to the CSP, set this value to false.


<b>WriteCertToCSP</b> affects the behavior of the following methods:

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
<pre>BOOL     bWriteCSP;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the WriteCertToCSP value
hr = pEnroll-&gt;get_WriteCertToCSP( &amp;bWriteCSP );
if (FAILED( hr ))
    printf("Failed get_WriteCertToCSP - %x\n", hr );
else
    printf( "WriteCertToCSP: %d\n", bWriteCSP );

// set the WriteCertToCSP value
hr = pEnroll-&gt;put_WriteCertToCSP( TRUE );
if (FAILED( hr ))
    printf("Failed put_WriteCertToCSP - %x\n", hr );
else
    printf( "WriteCertToCSP set to TRUE\n" );</pre>
</td>
</tr>
</table></span></div>


