---
UID: NF:securitybaseapi.AddAce
title: AddAce function (securitybaseapi.h)
description: Adds one or more access control entries (ACEs) to a specified access control list (ACL).
helpviewer_keywords: ["AddAce","AddAce function [Security]","_win32_addace","security.addace","securitybaseapi/AddAce"]
old-location: security\addace.htm
tech.root: security
ms.assetid: f472d864-a273-49b5-b5e2-98772989971e
ms.date: 12/05/2018
ms.keywords: AddAce, AddAce function [Security], _win32_addace, security.addace, securitybaseapi/AddAce
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - AddAce
 - securitybaseapi/AddAce
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
 - AddAce
---

# AddAce function


## -description

The <b>AddAce</b> function adds one or more <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) to a specified <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pAcl [in, out]

A pointer to an 
ACL. This function adds an ACE to this ACL.

### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs. This value must be compatible with the <b>AceType</b> field of all ACEs in <i>pAceList</i>. 
 Otherwise, the function will fail and set the last error to ERROR_INVALID_PARAMETER.

### -param dwStartingAceIndex [in]

Specifies the position in the ACL's list of ACEs at which to add new ACEs. A value of zero inserts the ACEs at the beginning of the list. A value of MAXDWORD appends the ACEs to the end of the list.

### -param pAceList [in]

A pointer to a list of one or more ACEs to be added to the specified ACL. The ACEs in the list must be stored contiguously.

### -param nAceListLength [in]

Specifies the size, in bytes, of the input buffer pointed to by the <i>pAceList</i> parameter.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

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

Applications frequently use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace">FindFirstFreeAce</a> and 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a> functions when using the <b>AddAce</b> function to manipulate an ACL. In addition, the 
<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a> structure retrieved by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a> function contains the size of the ACL and the number of ACEs it contains.


#### Examples

For an example that uses this function, see <a href="/previous-versions/aa379608(v=vs.85)">Starting an Interactive Client Process</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl_size_information">ACL_SIZE_INFORMATION</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessace">AddAuditAccessAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-deleteace">DeleteAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace">FindFirstFreeAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>