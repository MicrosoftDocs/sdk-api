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

# ICspInformation::get_KeySpec


## -description


The <b>KeySpec</b> property retrieves a value that specifies the intended use of the algorithms supported by the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The value retrieved can be 0, 1, 2, or 3. If the value is 0 (XCN_AT_NONE), the provider is a Cryptography API: Next Generation (CNG) provider. The values associated with the providers distributed by Microsoft are listed in the following table. Some of these providers may not be included on all operating systems and others may be included instead.<table>
<tr>
<th>Provider</th>
<th>KeySpec value</th>
</tr>
<tr>
<td>
Microsoft Software Key Storage Provider

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Microsoft Smart Card Key Storage Provider

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Microsoft Base Cryptographic Provider v1.0

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Base DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Base DSS Cryptographic Provider

</td>
<td>
2

</td>
</tr>
<tr>
<td>
Microsoft Base Smart Card Crypto Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft DH Schannel Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced Cryptographic Provider v1.0

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft Enhanced RSA and AES Cryptographic Provider

</td>
<td>
3

</td>
</tr>
<tr>
<td>
Microsoft RSA Schannel Cryptographic Provider

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Microsoft Strong Cryptographic Provider

</td>
<td>
3

</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

