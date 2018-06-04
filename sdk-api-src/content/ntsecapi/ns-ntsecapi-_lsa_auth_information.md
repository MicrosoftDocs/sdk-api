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

# _LSA_AUTH_INFORMATION structure


## -description


The <b>LSA_AUTH_INFORMATION</b> structure contains authentication information for a trusted domain.


## -struct-fields




### -field LastUpdateTime

A 
<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that uses the Coordinated Universal Time (Greenwich Mean Time) format to indicate the time that this value was set. For more information about Coordinated Universal Time, see the 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -field AuthType

Specifies one of the following values to indicate the type of authentication information in the <b>AuthInfo</b> buffer. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_AUTH_TYPE_NONE"></a><a id="trust_auth_type_none"></a><dl>
<dt><b>TRUST_AUTH_TYPE_NONE</b></dt>
</dl>
</td>
<td width="60%">
The format is unknown and will be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_AUTH_TYPE_NT4OWF"></a><a id="trust_auth_type_nt4owf"></a><dl>
<dt><b>TRUST_AUTH_TYPE_NT4OWF</b></dt>
</dl>
</td>
<td width="60%">
The Windows NT 4.0 one-way format (OWF) of a plaintext password. Note that you cannot derive the clear password back from the OWF form of the password. 




The system sets this information.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_AUTH_TYPE_CLEAR"></a><a id="trust_auth_type_clear"></a><dl>
<dt><b>TRUST_AUTH_TYPE_CLEAR</b></dt>
</dl>
</td>
<td width="60%">
Plaintext password to use for the trust.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_AUTH_TYPE_VERSION"></a><a id="trust_auth_type_version"></a><dl>
<dt><b>TRUST_AUTH_TYPE_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Plaintext password version number.

</td>
</tr>
</table>
 


### -field AuthInfoLength

Specifies the size, in bytes, of the <b>AuthInfo</b> member.


### -field AuthInfo

Pointer to an array of bytes that contains the type of authentication information indicated by the <b>AuthType</b> member.

