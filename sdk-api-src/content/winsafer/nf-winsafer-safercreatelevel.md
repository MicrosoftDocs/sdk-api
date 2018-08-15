---
UID: NF:winsafer.SaferCreateLevel
title: SaferCreateLevel function
author: windows-sdk-content
description: Opens a SAFER_LEVEL_HANDLE.
old-location: security\safercreatelevel.htm
old-project: secmgmt
ms.assetid: 7deb1365-5355-4983-900b-8e4fed009403
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SAFER_LEVELID_CONSTRAINED, SAFER_LEVELID_DISALLOWED, SAFER_LEVELID_FULLYTRUSTED, SAFER_LEVELID_NORMALUSER, SAFER_LEVELID_UNTRUSTED, SAFER_LEVEL_OPEN, SAFER_SCOPEID_MACHINE, SAFER_SCOPEID_USER, SaferCreateLevel, SaferCreateLevel function [Security], _mnp_safercreatelevel, security.safercreatelevel, winsafer/SaferCreateLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsafer.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SAFER_POLICY_INFO_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
 - SaferCreateLevel
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



