---
UID: NF:xenroll.ICEnroll2.get_WriteCertToUserDS
title: ICEnroll2::get_WriteCertToUserDS
author: windows-sdk-content
description: Sets or retrieves a Boolean value that determines whether the certificate is written to the user's Active Directory store.
old-location: security\icenroll4_writecerttouserds.htm
tech.root: seccrypto
ms.assetid: 8c80f6b9-f5f7-4fa1-9cb5-db19cdc9ec25
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CEnroll object [Security],WriteCertToUserDS property, ICEnroll2 interface [Security],WriteCertToUserDS property, ICEnroll2.WriteCertToUserDS, ICEnroll2.get_WriteCertToUserDS, ICEnroll2::get_WriteCertToUserDS, ICEnroll2::put_WriteCertToUserDS, ICEnroll3 interface [Security],WriteCertToUserDS property, ICEnroll3.WriteCertToUserDS, ICEnroll3::get_WriteCertToUserDS, ICEnroll3::put_WriteCertToUserDS, ICEnroll4 interface [Security],WriteCertToUserDS property, ICEnroll4.WriteCertToUserDS, ICEnroll4::WriteCertToUserDS, ICEnroll4::get_WriteCertToUserDS, ICEnroll4::put_WriteCertToUserDS, WriteCertToUserDS property [Security], WriteCertToUserDS property [Security],CEnroll object, WriteCertToUserDS property [Security],ICEnroll2 interface, WriteCertToUserDS property [Security],ICEnroll3 interface, WriteCertToUserDS property [Security],ICEnroll4 interface, get_WriteCertToUserDS, security.icenroll4_writecerttouserds, xenroll/ICEnroll2::WriteCertToUserDS, xenroll/ICEnroll2::get_WriteCertToUserDS, xenroll/ICEnroll2::put_WriteCertToUserDS, xenroll/ICEnroll3::WriteCertToUserDS, xenroll/ICEnroll3::get_WriteCertToUserDS, xenroll/ICEnroll3::put_WriteCertToUserDS, xenroll/ICEnroll4::WriteCertToUserDS, xenroll/ICEnroll4::get_WriteCertToUserDS, xenroll/ICEnroll4::put_WriteCertToUserDS
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
 - ICEnroll4.WriteCertToUserDS
 - ICEnroll4.get_WriteCertToUserDS
 - ICEnroll4.put_WriteCertToUserDS
 - ICEnroll3.WriteCertToUserDS
 - ICEnroll3.get_WriteCertToUserDS
 - ICEnroll3.put_WriteCertToUserDS
 - ICEnroll2.WriteCertToUserDS
 - ICEnroll2.get_WriteCertToUserDS
 - ICEnroll2.put_WriteCertToUserDS
 - CEnroll.WriteCertToUserDS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


