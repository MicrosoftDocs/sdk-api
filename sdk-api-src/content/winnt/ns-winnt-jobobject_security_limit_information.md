---
UID: NS:winnt._JOBOBJECT_SECURITY_LIMIT_INFORMATION
title: JOBOBJECT_SECURITY_LIMIT_INFORMATION (winnt.h)
description: Contains the security limitations for a job object.
helpviewer_keywords: ["*PJOBOBJECT_SECURITY_LIMIT_INFORMATION","JOBOBJECT_SECURITY_LIMIT_INFORMATION","JOBOBJECT_SECURITY_LIMIT_INFORMATION structure","JOB_OBJECT_SECURITY_FILTER_TOKENS","JOB_OBJECT_SECURITY_NO_ADMIN","JOB_OBJECT_SECURITY_ONLY_TOKEN","JOB_OBJECT_SECURITY_RESTRICTED_TOKEN","PJOBOBJECT_SECURITY_LIMIT_INFORMATION","PJOBOBJECT_SECURITY_LIMIT_INFORMATION structure pointer","_JOBOBJECT_SECURITY_LIMIT_INFORMATION","_win32_jobobject_security_limit_information_str","base.jobobject_security_limit_information_str","winnt/JOBOBJECT_SECURITY_LIMIT_INFORMATION","winnt/PJOBOBJECT_SECURITY_LIMIT_INFORMATION"]
old-location: base\jobobject_security_limit_information_str.htm
tech.root: backup
ms.assetid: 148f76b2-809b-4306-a943-bcc04aea547b
ms.date: 12/05/2018
ms.keywords: '*PJOBOBJECT_SECURITY_LIMIT_INFORMATION, JOBOBJECT_SECURITY_LIMIT_INFORMATION, JOBOBJECT_SECURITY_LIMIT_INFORMATION structure, JOB_OBJECT_SECURITY_FILTER_TOKENS, JOB_OBJECT_SECURITY_NO_ADMIN, JOB_OBJECT_SECURITY_ONLY_TOKEN, JOB_OBJECT_SECURITY_RESTRICTED_TOKEN, PJOBOBJECT_SECURITY_LIMIT_INFORMATION, PJOBOBJECT_SECURITY_LIMIT_INFORMATION structure pointer, _JOBOBJECT_SECURITY_LIMIT_INFORMATION, _win32_jobobject_security_limit_information_str, base.jobobject_security_limit_information_str, winnt/JOBOBJECT_SECURITY_LIMIT_INFORMATION, winnt/PJOBOBJECT_SECURITY_LIMIT_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: JOBOBJECT_SECURITY_LIMIT_INFORMATION, *PJOBOBJECT_SECURITY_LIMIT_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _JOBOBJECT_SECURITY_LIMIT_INFORMATION
 - winnt/_JOBOBJECT_SECURITY_LIMIT_INFORMATION
 - PJOBOBJECT_SECURITY_LIMIT_INFORMATION
 - winnt/PJOBOBJECT_SECURITY_LIMIT_INFORMATION
 - JOBOBJECT_SECURITY_LIMIT_INFORMATION
 - winnt/JOBOBJECT_SECURITY_LIMIT_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_SECURITY_LIMIT_INFORMATION
---

# JOBOBJECT_SECURITY_LIMIT_INFORMATION structure


## -description

<p class="CCE_Message">[JOBOBJECT_SECURITY_LIMIT_INFORMATION is available for use in the operating systems specified in the Requirements section. Support for this structure was removed starting with Windows Vista. For information, see Remarks.]

Contains the security limitations for a job object.

## -struct-fields

### -field SecurityLimitFlags

The security limitations for the job. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_SECURITY_FILTER_TOKENS"></a><a id="job_object_security_filter_tokens"></a><dl>
<dt><b>JOB_OBJECT_SECURITY_FILTER_TOKENS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Applies a filter to the token when a process impersonates a client. Requires at least one of the following members to be set: <b>SidsToDisable</b>, <b>PrivilegesToDelete</b>, or <b>RestrictedSids</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_SECURITY_NO_ADMIN"></a><a id="job_object_security_no_admin"></a><dl>
<dt><b>JOB_OBJECT_SECURITY_NO_ADMIN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Prevents any process in the job from using a token that specifies the local administrators group.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_SECURITY_ONLY_TOKEN"></a><a id="job_object_security_only_token"></a><dl>
<dt><b>JOB_OBJECT_SECURITY_ONLY_TOKEN</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Forces processes in the job to run under a specific token. Requires a token handle in the <b>JobToken</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="JOB_OBJECT_SECURITY_RESTRICTED_TOKEN"></a><a id="job_object_security_restricted_token"></a><dl>
<dt><b>JOB_OBJECT_SECURITY_RESTRICTED_TOKEN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Prevents any process in the job from using a token that was not created with the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a> function.

</td>
</tr>
</table>

### -field JobToken

A handle to the primary token that represents a user. The handle must have TOKEN_ASSIGN_PRIMARY access. 




If the token was created with 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, all processes in the job are limited to that token or a further restricted token. Otherwise, the caller must have the SE_ASSIGNPRIMARYTOKEN_NAME privilege.

### -field SidsToDisable

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies the SIDs to disable for access checking, if <b>SecurityLimitFlags</b> is JOB_OBJECT_SECURITY_FILTER_TOKENS. 




This member can be NULL if you do not want to disable any SIDs.

### -field PrivilegesToDelete

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that specifies the privileges to delete from the token, if <b>SecurityLimitFlags</b> is JOB_OBJECT_SECURITY_FILTER_TOKENS. 




This member can be NULL if you do not want to delete any privileges.

### -field RestrictedSids

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that specifies the deny-only SIDs that will be added to the access token, if <b>SecurityLimitFlags</b> is JOB_OBJECT_SECURITY_FILTER_TOKENS. 




This member can be NULL if you do not want to specify any deny-only SIDs.

## -remarks

After security limitations are placed on processes in a job, they cannot be revoked.

Starting with Windows Vista, you must set security limitations individually for each process associated with a job object, rather than setting them for the job object by using <a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>. For information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>