---
UID: NF:securitybaseapi.AddAccessDeniedAceEx
title: AddAccessDeniedAceEx function (securitybaseapi.h)
description: Adds an access-denied access control entry (ACE) to the end of a discretionary access control list (DACL).helpviewer_keywords: ["AddAccessDeniedAceEx","AddAccessDeniedAceEx function [Security]","CONTAINER_INHERIT_ACE","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","_win32_addaccessdeniedaceex","security.addaccessdeniedaceex","securitybaseapi/AddAccessDeniedAceEx"]
old-location: security\addaccessdeniedaceex.htm
tech.root: SecAuthZ
ms.assetid: e353c88c-f82e-40c0-b676-38f0060acc81
ms.date: 12/05/2018
ms.keywords: AddAccessDeniedAceEx, AddAccessDeniedAceEx function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, _win32_addaccessdeniedaceex, security.addaccessdeniedaceex, securitybaseapi/AddAccessDeniedAceEx
f1_keywords:
- securitybaseapi/AddAccessDeniedAceEx
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
- API-MS-Win-Security-base-l1-1-0.dll
- API-MS-Win-Security-base-l1-2-0.dll
- MinKernelBase.dll
- API-MS-Win-Security-Base-L1-2-1.dll
api_name:
- AddAccessDeniedAceEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddAccessDeniedAceEx function


## -description


The <b>AddAccessDeniedAceEx</b> function adds an access-denied <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to the end of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL).


## -parameters




### -param pAcl [in, out]

A pointer to a DACL. The <b>AddAccessDeniedAceEx</b> function adds an access-denied ACE to the end of this DACL. The ACE is in the form of an 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a> structure.


### -param dwAceRevision [in]

Specifies the revision level of the DACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the DACL contains object-specific ACEs.


### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure of the new ACE. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs, while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by noncontainer objects.

</td>
</tr>
</table>
 


### -param AccessMask [in]

A set of bit flags that use the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> format to specify the access rights that the new ACE denies to the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).


### -param pSid [in]

A pointer to a 
SID  that identifies the user, group, or <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">logon session</a> to which the new ACE denies access.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

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
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>AceFlags</i> parameter is not valid.

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



Although the <b>AddAccessDeniedAceEx</b> function adds the new ACE to the end of the DACL, access-denied ACEs should appear at the beginning of a DACL. The caller must ensure that ACEs are added to the DACL in the correct order. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl">Order of ACEs in a DACL</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex">AddAccessAllowedAceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessaceex">AddAuditAccessAceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>
 

 

