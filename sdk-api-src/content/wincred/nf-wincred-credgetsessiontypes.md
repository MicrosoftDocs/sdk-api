---
UID: NF:wincred.CredGetSessionTypes
title: CredGetSessionTypes function (wincred.h)
description: The CredGetSessionTypes function returns the maximum persistence supported by the current logon session. A separate maximum persistence is returned for each credential type.
helpviewer_keywords: ["CRED_PERSIST_ENTERPRISE","CRED_PERSIST_LOCAL_MACHINE","CRED_PERSIST_NONE","CRED_PERSIST_SESSION","CredGetSessionTypes","CredGetSessionTypes function [Security]","_cred_credgetsessiontypes","security.credgetsessiontypes","wincred/CredGetSessionTypes"]
old-location: security\credgetsessiontypes.htm
tech.root: security
ms.assetid: 70f8d5e0-235b-4330-8add-566b41c91c17
ms.date: 12/05/2018
ms.keywords: CRED_PERSIST_ENTERPRISE, CRED_PERSIST_LOCAL_MACHINE, CRED_PERSIST_NONE, CRED_PERSIST_SESSION, CredGetSessionTypes, CredGetSessionTypes function [Security], _cred_credgetsessiontypes, security.credgetsessiontypes, wincred/CredGetSessionTypes
req.header: wincred.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredGetSessionTypes
 - wincred/CredGetSessionTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredGetSessionTypes
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

This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function can be called to get a more specific status code. The following status code can be returned:

ERROR_NO_SUCH_LOGON_SESSION

The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.