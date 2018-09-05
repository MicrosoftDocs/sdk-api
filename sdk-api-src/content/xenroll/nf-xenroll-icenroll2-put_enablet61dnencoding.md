---
UID: NF:xenroll.ICEnroll2.put_EnableT61DNEncoding
title: ICEnroll2::put_EnableT61DNEncoding
author: windows-sdk-content
description: The EnableT61DNEncoding property of ICEnroll4 sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a Unicode string.
old-location: security\icenroll4_enablet61dnencoding.htm
old-project: seccrypto
ms.assetid: ff8fe103-0303-4f40-af25-efa50155c36f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CEnroll object [Security],EnableT61DNEncoding property, EnableT61DNEncoding property [Security], EnableT61DNEncoding property [Security],CEnroll object, EnableT61DNEncoding property [Security],ICEnroll2 interface, EnableT61DNEncoding property [Security],ICEnroll3 interface, EnableT61DNEncoding property [Security],ICEnroll4 interface, ICEnroll2 interface [Security],EnableT61DNEncoding property, ICEnroll2.EnableT61DNEncoding, ICEnroll2.put_EnableT61DNEncoding, ICEnroll2::get_EnableT61DNEncoding, ICEnroll2::put_EnableT61DNEncoding, ICEnroll3 interface [Security],EnableT61DNEncoding property, ICEnroll3.EnableT61DNEncoding, ICEnroll3::get_EnableT61DNEncoding, ICEnroll3::put_EnableT61DNEncoding, ICEnroll4 interface [Security],EnableT61DNEncoding property, ICEnroll4.EnableT61DNEncoding, ICEnroll4::EnableT61DNEncoding, ICEnroll4::get_EnableT61DNEncoding, ICEnroll4::put_EnableT61DNEncoding, put_EnableT61DNEncoding, security.icenroll4_enablet61dnencoding, xenroll/ICEnroll2::EnableT61DNEncoding, xenroll/ICEnroll2::get_EnableT61DNEncoding, xenroll/ICEnroll2::put_EnableT61DNEncoding, xenroll/ICEnroll3::EnableT61DNEncoding, xenroll/ICEnroll3::get_EnableT61DNEncoding, xenroll/ICEnroll3::put_EnableT61DNEncoding, xenroll/ICEnroll4::EnableT61DNEncoding, xenroll/ICEnroll4::get_EnableT61DNEncoding, xenroll/ICEnroll4::put_EnableT61DNEncoding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.EnableT61DNEncoding
 - ICEnroll4.get_EnableT61DNEncoding
 - ICEnroll4.put_EnableT61DNEncoding
 - ICEnroll3.EnableT61DNEncoding
 - ICEnroll3.get_EnableT61DNEncoding
 - ICEnroll3.put_EnableT61DNEncoding
 - ICEnroll2.EnableT61DNEncoding
 - ICEnroll2.get_EnableT61DNEncoding
 - ICEnroll2.put_EnableT61DNEncoding
 - CEnroll.EnableT61DNEncoding
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll2::put_EnableT61DNEncoding


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnableT61DNEncoding</b> property sets or retrieves a Boolean value that determines whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.

 A T61 character is 8 bits, hence all Unicode characters to be encoded must be less than or equal to 0xFF.  This property was first defined in the <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks




The <b>EnableT61DNEncoding</b> property affects the behavior of the following methods:

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
<pre>BOOL     bT61DN;
HRESULT  hr;


// pEnroll is a previously instantiated ICEnroll2 interface pointer.
// Get the EnableT61DNEncoding Boolean value.

hr = pEnroll-&gt;get_EnableT61DNEncoding( &amp;bT61DN );
if ( FAILED ( hr ) )
    printf("Failed get_EnableT61DNEncoding - %x\n", hr );
else
    printf( "T61DNEncoding: %s\n", 
             ( bT61DN ? "Enabled" : "Disabled" ) );


// Set the EnableT61DNEncoding value.

hr = pEnroll-&gt;put_EnableT61DNEncoding( TRUE );
if ( FAILED ( hr ) )
    printf("Failed Setting EnableT61DNEncoding - %x\n", hr );
else
    printf( "EnableT61DNEncoding was set to TRUE\n" );</pre>
</td>
</tr>
</table></span></div>


