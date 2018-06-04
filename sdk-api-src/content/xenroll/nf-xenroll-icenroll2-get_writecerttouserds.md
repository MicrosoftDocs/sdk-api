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

# ICEnroll2::get_WriteCertToUserDS


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToUserDS</b> property sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory  store.

 This property should not need to be modified by most applications. This property was first defined in the <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks




<b>WriteCertToUserDS</b> affects the behavior of the following methods:

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
<pre>BOOL     bWriteUserDS;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll2 interface pointer

// get the WriteCertToUserDS value
hr = pEnroll-&gt;get_WriteCertToUserDS( &amp;bWriteUserDS );
if (FAILED( hr ))
    printf("Failed get_WriteCertToUserDS - %x\n", hr );
else
    printf( "WriteCertToUserDS: %d\n", bWriteUserDS );

// set the WriteCertToUserDS value
hr = pEnroll-&gt;put_WriteCertToUserDS( TRUE );
if (FAILED( hr ))
    printf("Failed put_WriteCertToUserDS - %x\n", hr );
else
    printf( "WriteCertToUserDS set to TRUE\n" );</pre>
</td>
</tr>
</table></span></div>


