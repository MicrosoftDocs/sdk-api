---
UID: NC:ntsecpkg.LSA_CREATE_LOGON_SESSION
title: LSA_CREATE_LOGON_SESSION (ntsecpkg.h)
description: Creates logon sessions.
helpviewer_keywords: ["CreateLogonSession","CreateLogonSession callback function [Security]","LSA_CREATE_LOGON_SESSION","LSA_CREATE_LOGON_SESSION callback","_lsa_createlogonsession","ntsecpkg/CreateLogonSession","security.createlogonsession"]
old-location: security\createlogonsession.htm
tech.root: security
ms.assetid: 383c935c-a1f2-4d1b-bb02-e7e37f154771
ms.date: 12/05/2018
ms.keywords: CreateLogonSession, CreateLogonSession callback function [Security], LSA_CREATE_LOGON_SESSION, LSA_CREATE_LOGON_SESSION callback, _lsa_createlogonsession, ntsecpkg/CreateLogonSession, security.createlogonsession
req.header: ntsecpkg.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_CREATE_LOGON_SESSION
 - ntsecpkg/LSA_CREATE_LOGON_SESSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - CreateLogonSession
---

# LSA_CREATE_LOGON_SESSION callback function


## -description

Creates logon sessions.

The logon session is identified by a unique logon ID (
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>) assigned to the logon session.

## -parameters

### -param LogonId [in]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure to be assigned to the new logon session. An authentication package calls 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocatelocallyuniqueid">AllocateLocallyUniqueId</a> in order to generate this ID.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOGON_SESSION_COLLISION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon ID is already in use by another logon session.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

If an authentication package creates extraneous logon sessions while determining whether to authenticate the user, it should delete them by calling 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session">DeleteLogonSession</a>. If the authentication fails, the authentication package should delete all related logon sessions.

Because logon sessions use memory in the kernel, it is important to delete any unused or discarded logon sessions.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_delete_logon_session">DeleteLogonSession</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>