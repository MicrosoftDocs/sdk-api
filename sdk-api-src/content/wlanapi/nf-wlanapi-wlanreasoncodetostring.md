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

# WlanReasonCodeToString function


## -description


The <b>WlanReasonCodeToString</b> function retrieves a  string that describes a specified reason code.


## -parameters




### -param dwReasonCode [in]

A <a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a> value of which the string description is requested.


### -param dwBufferSize [in]

The size of the buffer used to store the string, in <b>WCHAR</b>.  If the reason code string is longer than the buffer, it will be truncated and NULL-terminated. If <i>dwBufferSize</i> is larger than the actual amount of memory allocated to <i>pStringBuffer</i>, then an access violation will occur in the calling program.


### -param pStringBuffer [in]

Pointer to a buffer that will receive the string. The caller must allocate memory to <i>pStringBuffer</i> before calling <b>WlanReasonCodeToString</b>.


### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


## -returns



If the function succeeds, the return value is a pointer to a constant string.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if any of the following conditions occur:<ul>
<li><i>dwBufferSize</i> is 0.</li>
<li><i>pStringBuffer</i> is <b>NULL</b>.</li>
<li><i>pReserved</i> is not <b>NULL</b>.</li>
</ul>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Various RPC and other error codes. Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7b267f0b-b3f7-4729-bab4-de3bdd0a35a2">WLAN_REASON_CODE</a>
 

 

