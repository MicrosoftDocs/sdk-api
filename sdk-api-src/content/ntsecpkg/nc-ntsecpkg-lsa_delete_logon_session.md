---
UID: NC:ntsecpkg.LSA_DELETE_LOGON_SESSION
title: LSA_DELETE_LOGON_SESSION (ntsecpkg.h)
description: Cleans up any logon sessions created while determining whether a user's authentication information is legitimate.
helpviewer_keywords: ["DeleteLogonSession","DeleteLogonSession callback function [Security]","LSA_DELETE_LOGON_SESSION","LSA_DELETE_LOGON_SESSION callback","_lsa_deletelogonsession","ntsecpkg/DeleteLogonSession","security.deletelogonsession"]
old-location: security\deletelogonsession.htm
tech.root: security
ms.assetid: 72b9451c-8a94-4e64-bd78-0afef210671c
ms.date: 12/05/2018
ms.keywords: DeleteLogonSession, DeleteLogonSession callback function [Security], LSA_DELETE_LOGON_SESSION, LSA_DELETE_LOGON_SESSION callback, _lsa_deletelogonsession, ntsecpkg/DeleteLogonSession, security.deletelogonsession
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
 - LSA_DELETE_LOGON_SESSION
 - ntsecpkg/LSA_DELETE_LOGON_SESSION
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
 - DeleteLogonSession
---

# LSA_DELETE_LOGON_SESSION callback function


## -description

Cleans up any logon sessions created while determining whether a user's authentication information is legitimate.

If the authentication fails, the authentication package should delete all related logon sessions.

## -parameters

### -param LogonId [in]

Pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure containing the session ID of logon session to delete.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_LOGON_SESSION_STATE</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session has a reference count value that prevents it from being deleted. This is a serious problem, caused by both the operating system and authentication package believing they have authority over the logon session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session could not be found.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

Because logon sessions use up memory in the kernel, any unused or discarded logon sessions should be deleted. However, logon sessions should not be deleted after a logon ID for the session has been returned to the LSA. After the LSA has been given a logon ID (for example, as a result of a 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user">LsaApLogonUser</a> call), the LSA assumes it is responsible for the logon session and will delete it when the operating system no longer needs it. At this time, the LSA calls 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_terminated">LsaApLogonTerminated</a> to notify the authentication package that the session has been deleted.

In contrast, authentication packages are not notified when a logon session is deleted with <b>DeleteLogonSession</b>.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_logon_session">CreateLogonSession</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_dispatch_table">LSA_DISPATCH_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>