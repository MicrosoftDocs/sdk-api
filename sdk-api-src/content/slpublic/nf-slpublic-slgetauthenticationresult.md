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

# SLGetAuthenticationResult function


## -description


Gets the authentication results.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the authentication result.


### -param ppbValue [out]

Type: <b>PBYTE*</b>

A pointer to the authentication result. When finished using the memory, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_MISMATCHED_KEY</b></dt>
<dt>0xC004F078</dt>
</dl>
</td>
<td width="60%">
The key used in the <a href="https://msdn.microsoft.com/68906873-6c49-4221-ad87-1e1f1463c0d4">SLSetAuthenticationData</a> function call is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_CANT_VERIFY</b></dt>
<dt>0xC004F07A</dt>
</dl>
</td>
<td width="60%">
The authentication cannot be completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_CHALLENGE_NOT_SET</b></dt>
<dt>0xC004F079</dt>
</dl>
</td>
<td width="60%">
The authentication data (challenge) is not set.

</td>
</tr>
</table>
 



