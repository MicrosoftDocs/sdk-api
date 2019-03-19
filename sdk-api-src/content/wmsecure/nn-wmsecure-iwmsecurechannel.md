---
UID: NN:wmsecure.IWMSecureChannel
title: IWMSecureChannel (wmsecure.h)
author: windows-sdk-content
description: The IWMSecureChannel interface provides methods that allow two DLLs to validate each other and perform secure communication.
old-location: wmformat\iwmsecurechannel.htm
tech.root: wmformat
ms.assetid: ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMSecureChannel, IWMSecureChannel interface [windows Media Format], IWMSecureChannel interface [windows Media Format],described, wmformat.iwmsecurechannel, wmsecure/IWMSecureChannel
ms.topic: interface
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSecureChannel interface


## -description


<p class="CCE_Message">[<b>IWMSecureChannel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>IWMSecureChannel</b> interface provides methods that allow two DLLs to validate
 each other and perform secure communication.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMSecureChannel</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd743287(v=VS.85).aspx">IWMAuthorizer</a>. <b>IWMSecureChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMSecureChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743706(v=VS.85).aspx">WMSC_AddCertificate</a>
</td>
<td align="left" width="63%">
Adds certificates that this object can present to other securechannel objects.
     If no certs are added, then this object can only connect to objects with
     no signatures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743707(v=VS.85).aspx">WMSC_AddSignature</a>
</td>
<td align="left" width="63%">
    Adds signatures that this object will look for when trying to connect. 
     If no signatures are added, then this object will connect to any other object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743708(v=VS.85).aspx">WMSC_Connect</a>
</td>
<td align="left" width="63%">
Initializes the secure connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743709(v=VS.85).aspx">WMSC_Decrypt</a>
</td>
<td align="left" width="63%">
Decrypts data across DLL boundaries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743710(v=VS.85).aspx">WMSC_Disconnect</a>
</td>
<td align="left" width="63%">
Destroys the secure connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743711(v=VS.85).aspx">WMSC_Encrypt</a>
</td>
<td align="left" width="63%">
Encrypts data across DLL boundaries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743712(v=VS.85).aspx">WMSC_GetValidCertificate</a>
</td>
<td align="left" width="63%">
 Returns a copy of the certificate that was used provided by the other side
     of the connection.  Also returns the index of the signature that validated
     that certificate.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743713(v=VS.85).aspx">WMSC_IsConnected</a>
</td>
<td align="left" width="63%">
Checks to see if the secure connection is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743714(v=VS.85).aspx">WMSC_Lock</a>
</td>
<td align="left" width="63%">
Used to lock access to the secure connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743715(v=VS.85).aspx">WMSC_SetSharedData</a>
</td>
<td align="left" width="63%">
Used during the connection negotiation process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd743716(v=VS.85).aspx">WMSC_Unlock</a>
</td>
<td align="left" width="63%">
Used to unlock access to the secure connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743287(v=VS.85).aspx">IWMAuthorizer</a>
 

 

