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

# SaferCreateLevel function


## -description


The <b>SaferCreateLevel</b> function opens a SAFER_LEVEL_HANDLE.


## -parameters




### -param dwScopeId [in]

The scope of the level to be created. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_SCOPEID_MACHINE"></a><a id="safer_scopeid_machine"></a><dl>
<dt><b>SAFER_SCOPEID_MACHINE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The scope of the created level is by computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_SCOPEID_USER"></a><a id="safer_scopeid_user"></a><dl>
<dt><b>SAFER_SCOPEID_USER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The scope of the created level is by user.

</td>
</tr>
</table>
 


### -param dwLevelId [in]

The level of the handle to be opened. The following table shows the possible values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVELID_CONSTRAINED"></a><a id="safer_levelid_constrained"></a><dl>
<dt><b>SAFER_LEVELID_CONSTRAINED</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
Software cannot access certain resources, such as cryptographic keys and credentials, regardless of the user rights of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVELID_DISALLOWED"></a><a id="safer_levelid_disallowed"></a><dl>
<dt><b>SAFER_LEVELID_DISALLOWED</b></dt>
<dt>0x00000</dt>
</dl>
</td>
<td width="60%">
Software will not run, regardless of the user rights of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVELID_FULLYTRUSTED"></a><a id="safer_levelid_fullytrusted"></a><dl>
<dt><b>SAFER_LEVELID_FULLYTRUSTED</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
Software user rights are determined by the user rights of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVELID_NORMALUSER"></a><a id="safer_levelid_normaluser"></a><dl>
<dt><b>SAFER_LEVELID_NORMALUSER</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
Allows programs to execute as a user that does not have <b>Administrator</b> or <b>Power User</b> user rights. Software can access resources accessible by normal users.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVELID_UNTRUSTED"></a><a id="safer_levelid_untrusted"></a><dl>
<dt><b>SAFER_LEVELID_UNTRUSTED</b></dt>
<dt>0x01000</dt>
</dl>
</td>
<td width="60%">
Allows programs to execute with access only to resources granted to open well-known groups, blocking access to <b>Administrator</b> and <b>Power User</b> privileges and personally granted rights.

</td>
</tr>
</table>
 


### -param OpenFlags [in]

This can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_LEVEL_OPEN"></a><a id="safer_level_open"></a><dl>
<dt><b>SAFER_LEVEL_OPEN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 


### -param pLevelHandle [out]

The returned SAFER_LEVEL_HANDLE. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/8daffb35-5bb0-45b3-aff1-a8ea6a142ba5">SaferCloseLevel</a> function.


### -param lpReserved

This parameter is reserved for future use. Set it to <b>NULL</b>.


## -returns



Returns nonzero if successful or zero otherwise. 
						

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



