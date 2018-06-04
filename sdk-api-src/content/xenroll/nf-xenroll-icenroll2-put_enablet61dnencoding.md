---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


