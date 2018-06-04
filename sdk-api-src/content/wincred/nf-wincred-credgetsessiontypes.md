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

# CredGetSessionTypes function


## -description


The <b>CredGetSessionTypes</b> function returns the maximum persistence supported by the current logon session. A separate maximum persistence is returned for each credential type.


## -parameters




### -param MaximumPersistCount [in]

Number of elements in the <i>MaximumPersist</i> array. Use CRED_TYPE_MAXIMUM to return all of the currently defined credential types.


### -param MaximumPersist [out]

Pointer to an array to return the persistence values in. The passed in array should be <i>MaximumPersistCount</i> elements long. On return, each element specifies the maximum persistence supported by the corresponding credential type.

The caller should use one of the following defines to index into the array:

<ul>
<li>CRED_TYPE_GENERIC</li>
<li>CRED_TYPE_DOMAIN_PASSWORD</li>
<li>CRED_TYPE_DOMAIN_CERTIFICATE</li>
</ul>
That is, <i>MaximumPersist</i>[CRED_TYPE_GENERIC] specifies the maximum persistence supported for generic credentials. 


The following values can be returned in each element of the array.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_NONE"></a><a id="cred_persist_none"></a><dl>
<dt><b>CRED_PERSIST_NONE</b></dt>
</dl>
</td>
<td width="60%">
No credential can be stored. This value will be returned if the credential type is not supported or has been disabled by policy.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_SESSION"></a><a id="cred_persist_session"></a><dl>
<dt><b>CRED_PERSIST_SESSION</b></dt>
</dl>
</td>
<td width="60%">
Only a session-specific credential can be stored.

</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_LOCAL_MACHINE"></a><a id="cred_persist_local_machine"></a><dl>
<dt><b>CRED_PERSIST_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Session-specific and computer-specific credentials can be stored.


<b>Windows XP:  </b>This credential cannot be stored for sessions in which the profile is not loaded.



</td>
</tr>
<tr>
<td width="40%"><a id="CRED_PERSIST_ENTERPRISE"></a><a id="cred_persist_enterprise"></a><dl>
<dt><b>CRED_PERSIST_ENTERPRISE</b></dt>
</dl>
</td>
<td width="60%">
Any credential can be stored.


<b>Windows XP:  </b>This credential cannot be stored for sessions in which the profile is not loaded.



</td>
</tr>
</table>
 


## -returns



This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_NO_SUCH_LOGON_SESSION

The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.



