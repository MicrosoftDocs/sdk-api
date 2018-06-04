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

# IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm


## -description


Gets the cipher algorithm associated with the security settings. The cipher algorithm is used to encrypt and decrypt information sent on the ad hoc network associated with an interface.


## -parameters




### -param pCipher [in, out]

A pointer to a <a href="https://msdn.microsoft.com/2ea8173d-f528-4065-90ce-71a455a6b35f">DOT11_ADHOC_CIPHER_ALGORITHM</a> value that specifies the cipher algorithm.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>pCipher</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer <i>pCipher</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/55b78a98-ad25-4646-b325-73d770d602b3">IDot11AdHocSecuritySettings</a>



<a href="https://msdn.microsoft.com/87ba445a-1ad7-49da-aa61-ed72d118e517">IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm</a>
 

 

