---
UID: NF:securitybaseapi.AddAccessDeniedAce
title: AddAccessDeniedAce function (securitybaseapi.h)
description: Adds an access-denied access control entry (ACE) to an access control list (ACL). The access is denied to a specified security identifier (SID).
helpviewer_keywords: ["AddAccessDeniedAce","AddAccessDeniedAce function [Security]","_win32_addaccessdeniedace","security.addaccessdeniedace","securitybaseapi/AddAccessDeniedAce"]
old-location: security\addaccessdeniedace.htm
tech.root: security
ms.assetid: 5b4c4164-48f4-4cd5-b60e-554f2498d547
ms.date: 12/05/2018
ms.keywords: AddAccessDeniedAce, AddAccessDeniedAce function [Security], _win32_addaccessdeniedace, security.addaccessdeniedace, securitybaseapi/AddAccessDeniedAce
req.header: securitybaseapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddAccessDeniedAce
 - securitybaseapi/AddAccessDeniedAce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddAccessDeniedAce
---

# AddAccessDeniedAce function


## -description

The <b>AddAccessDeniedAce</b> function adds an access-denied <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). The access is denied to a specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

To control whether the new ACE can be inherited by child objects, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedaceex">AddAccessDeniedAceEx</a> function.

## -parameters

### -param pAcl [in, out]

A pointer to an 
ACL . This function adds an access-denied ACE to the end of this ACL. The ACE is in the form of an 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a> structure.

### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.

### -param AccessMask [in]

Specifies the mask of access rights being denied to the specified SID.

### -param pSid [in]

A pointer to the SID structure representing the user, group, or logon account being denied access.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALLOTTED_SPACE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACL</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not structurally valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified revision is not known or is incompatible with that of the ACL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The ACE was successfully added.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a> and <b>AddAccessDeniedAce</b> functions add a new ACE to the end of the list of ACEs for the ACL. These functions do not automatically place the new ACE in the proper canonical order. It is the caller's responsibility to ensure that the ACL is in canonical order by adding ACEs in the proper sequence.

The 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure placed in the ACE by the <b>AddAccessDeniedAce</b> function specifies a type and size, but provides no ACE flags.

The ACE added by <b>AddAccessDeniedAce</b> is not inheritable.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedaceex">AddAccessDeniedAceEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addace">AddAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessace">AddAuditAccessAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-deleteace">DeleteAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>