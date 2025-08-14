---
UID: NF:securitybaseapi.SetPrivateObjectSecurityEx
title: SetPrivateObjectSecurityEx function (securitybaseapi.h)
description: Modifies the security descriptor of a private object maintained by the resource manager calling this function.
helpviewer_keywords: ["SEF_AVOID_OWNER_CHECK","SEF_AVOID_OWNER_RESTRICTION","SEF_AVOID_PRIVILEGE_CHECK","SEF_DACL_AUTO_INHERIT","SEF_DEFAULT_GROUP_FROM_PARENT","SEF_DEFAULT_OWNER_FROM_PARENT","SEF_MACL_NO_EXECUTE_UP","SEF_MACL_NO_READ_UP","SEF_MACL_NO_WRITE_UP","SEF_SACL_AUTO_INHERIT","SetPrivateObjectSecurityEx","SetPrivateObjectSecurityEx function [Security]","_win32_setprivateobjectsecurityex","security.setprivateobjectsecurityex","securitybaseapi/SetPrivateObjectSecurityEx"]
old-location: security\setprivateobjectsecurityex.htm
tech.root: security
ms.assetid: eb3a751f-741e-448f-b812-5f16a4040b5e
ms.date: 12/05/2018
ms.keywords: SEF_AVOID_OWNER_CHECK, SEF_AVOID_OWNER_RESTRICTION, SEF_AVOID_PRIVILEGE_CHECK, SEF_DACL_AUTO_INHERIT, SEF_DEFAULT_GROUP_FROM_PARENT, SEF_DEFAULT_OWNER_FROM_PARENT, SEF_MACL_NO_EXECUTE_UP, SEF_MACL_NO_READ_UP, SEF_MACL_NO_WRITE_UP, SEF_SACL_AUTO_INHERIT, SetPrivateObjectSecurityEx, SetPrivateObjectSecurityEx function [Security], _win32_setprivateobjectsecurityex, security.setprivateobjectsecurityex, securitybaseapi/SetPrivateObjectSecurityEx
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
 - SetPrivateObjectSecurityEx
 - securitybaseapi/SetPrivateObjectSecurityEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - SetPrivateObjectSecurityEx
---

# SetPrivateObjectSecurityEx function


## -description

The <b>SetPrivateObjectSecurityEx</b> function modifies the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> of a private object maintained by the resource manager calling this function. The <b>SetPrivateObjectSecurityEx</b> function has a flags parameter that specifies whether the resource manager supports automatic inheritance of <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

## -parameters

### -param SecurityInformation [in]

The parts of the security descriptor to set. This value can be a combination of the 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags.

### -param ModificationDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. The parts of this security descriptor indicated by the <i>SecurityInformation</i> parameter are applied to the <i>ObjectsSecurityDescriptor</i> security descriptor.

### -param ObjectsSecurityDescriptor [in, out]

A pointer to a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. This security descriptor must be in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> form. **The memory for the security descriptor must be allocated from the process heap (GetProcessHeap) with the HeapAlloc function.**




On input, this is the current security descriptor of the private object. The function modifies it to produce the new security descriptor. If necessary, the <b>SetPrivateObjectSecurityEx</b> function allocates additional memory to produce a larger security descriptor.

### -param AutoInheritFlags [in]

Specifies automatic inheritance of ACEs. If the protected server does not implement automatic inheritance, it should specify zero; otherwise, it can specify a combination of the following values, defined in Winnt.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEF_DACL_AUTO_INHERIT"></a><a id="sef_dacl_auto_inherit"></a><dl>
<dt><b>SEF_DACL_AUTO_INHERIT</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The new <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) contains ACEs inherited from the DACL of 
        the object's parent, as well as any explicit ACEs specified in the DACL of 
        <i>ModificationDescriptor</i>. If this flag is not set, the new DACL does not inherit ACEs.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_SACL_AUTO_INHERIT"></a><a id="sef_sacl_auto_inherit"></a><dl>
<dt><b>SEF_SACL_AUTO_INHERIT</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The new <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) contains ACEs inherited from the SACL of 
        the security descriptor associated with the object's parent, as well as any explicit ACEs specified in the SACL of 
        <i>ModificationDescriptor</i>. If this flag is not set, the new SACL does not inherit ACEs.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_AVOID_PRIVILEGE_CHECK"></a><a id="sef_avoid_privilege_check"></a><dl>
<dt><b>SEF_AVOID_PRIVILEGE_CHECK</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The function does not perform privilege checking. If the <b>SEF_AVOID_OWNER_CHECK</b> flag is also set, the <i>Token</i> parameter can be <b>NULL</b>. Use this flag when implementing automatic inheritance to avoid checking privileges on each child updated.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_AVOID_OWNER_CHECK"></a><a id="sef_avoid_owner_check"></a><dl>
<dt><b>SEF_AVOID_OWNER_CHECK</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The function does not check the validity of the owner in the resultant <i>ObjectsSecurityDescriptor</i> as described in Remarks. If the <b>SEF_AVOID_PRIVILEGE_CHECK</b> flag is also set, the <i>Token</i> parameter can be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_DEFAULT_OWNER_FROM_PARENT"></a><a id="sef_default_owner_from_parent"></a><dl>
<dt><b>SEF_DEFAULT_OWNER_FROM_PARENT</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The owner of <i>ObjectsSecurityDescriptor</i> defaults to the owner of the object's parent. If this flag is not set, the owner of <i>ObjectsSecurityDescriptor</i> defaults to the owner of the token specified by the <i>Token</i> parameter. The owner of the token is specified in the token itself. In either case, if the <i>ModificationDescriptor</i> parameter is not <b>NULL</b>, the <i>ObjectsSecurityDescriptor</i> owner is set to the owner from <i>ModificationDescriptor</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_DEFAULT_GROUP_FROM_PARENT"></a><a id="sef_default_group_from_parent"></a><dl>
<dt><b>SEF_DEFAULT_GROUP_FROM_PARENT</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
The group of <i>ObjectsSecurityDescriptor</i> defaults to the group from the owner of the object's parent. If this flag is not set, the group of <i>ObjectsSecurityDescriptor</i> defaults to the group of the token specified by the <i>Token</i> parameter. The group of the token is specified in the token itself. In either case, if the <i>ModificationDescriptor</i> parameter is not <b>NULL</b>, the <i>ObjectsSecurityDescriptor</i> group is set to the group from <i>ModificationDescriptor</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_MACL_NO_WRITE_UP"></a><a id="sef_macl_no_write_up"></a><dl>
<dt><b>SEF_MACL_NO_WRITE_UP</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
A principal with a mandatory level lower than that of the object cannot write to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_MACL_NO_READ_UP"></a><a id="sef_macl_no_read_up"></a><dl>
<dt><b>SEF_MACL_NO_READ_UP</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
A principal with a mandatory level lower than that of the object cannot read the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_MACL_NO_EXECUTE_UP"></a><a id="sef_macl_no_execute_up"></a><dl>
<dt><b>SEF_MACL_NO_EXECUTE_UP</b></dt>
<dt>0x400</dt>
</dl>
</td>
<td width="60%">
A principal with a mandatory level lower than that of the object cannot execute the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_AVOID_OWNER_RESTRICTION"></a><a id="sef_avoid_owner_restriction"></a><dl>
<dt><b>SEF_AVOID_OWNER_RESTRICTION</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Any restrictions  specified by the
            owner of the object's parent that would limit the caller's ability to specify
            a DACL in the <i>ObjectsSecurityDescriptor</i> are ignored.

</td>
</tr>
</table>

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure that specifies the specific and standard access rights that correspond to each of the generic access rights.

### -param Token [in, optional]

Identifies the <a href="/windows/desktop/SecGloss/a-gly">access token</a> for the client on whose behalf the private object's security is being modified. This parameter is required to ensure that the client has provided a legitimate value for a new owner <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). The token must be open for TOKEN_QUERY access.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>AutoInheritFlags</i> parameter is zero, <b>SetPrivateObjectSecurityEx</b> is identical to the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a> function.

This function is intended for use by resource managers only. To implement the standard Windows access control semantics for updating security descriptors, a resource manager should verify that the following conditions are met before calling <b>SetPrivateObjectSecurityEx</b>:

<ul>
<li>If the object's owner is being set, the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must have either WRITE_OWNER permission or be the object's owner.</li>
<li>If the object's DACL is being set, the calling process must have either WRITE_DAC permission or be the object's owner.</li>
<li>If the object's SACL is being set, the SE_SECURITY_NAME privilege must be enabled for the calling process.</li>
</ul>
If the preceding conditions are not met, a call to this function does not fail, however, standard Windows access policy is not enforced.

The process calling this function should not be impersonating a client because clients do not typically have appropriate privileges required for underlying token operations.

If <i>AutoInheritFlags</i> specifies the SEF_DACL_AUTO_INHERIT bit, the function applies the following rules to the DACL to create the new security descriptor from the current descriptor:

<ul>
<li>If the SE_DACL_PROTECTED flag is not set in the control bits of  either the current security descriptor or the <i>ModificationDescriptor</i>, the function constructs the output security descriptor from the inherited ACEs of the current security descriptor and noninherited ACEs of <i>ModificationDescriptor</i>. That is, it is impossible to change an inherited ACE by changing the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) on an object. This behavior preserves the inherited ACEs as they were inherited from the parent container. 


An ACL editor should make inherited ACEs unavailable to prevent them from being modified.

</li>
<li>If SE_DACL_PROTECTED is set in 
      <i>ModificationDescriptor</i>, the current security descriptor is ignored. The output security descriptor is built as a copy of 
      <i>ModificationDescriptor</i> with any INHERITED_ACE bits turned off. 


Ideally an ACL editor should turn off the INHERITED_ACE bits that indicate to its caller that the ACEs inherited from the object's parent are now being explicitly set on the object.

</li>
<li>If SE_DACL_PROTECTED is set in the current security descriptor and not in 
      <i>ModificationDescriptor</i>, the current security descriptor is ignored. The output security descriptor is built as a copy of 
      <i>ModificationDescriptor</i>. It is the caller's responsibility to ensure that the correct ACEs have the INHERITED_ACE bit turned on.</li>
</ul>
If <i>AutoInheritFlags</i> specifies the SEF_SACL_AUTO_INHERIT bit, the function applies similar rules to the new SACL.

For both DACLs and SACLs, certain types of ACEs in the input <i>ObjectsSecurityDescriptor</i> and in <i>ModificationDescriptor</i> will be replaced by two ACEs in the output <i>ObjectsSecurityDescriptor</i>. Specifically, an inheritable ACE that contains at least one of the following mappable elements will result in two ACEs in the output <i>ObjectsSecurityDescriptor</i>. Mappable elements include:

<ul>
<li>Generic access rights in the <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure</li>
<li>Creator Owner SID or Creator Group SID as the ACE subject identifier</li>
</ul>
ACEs with any of these mappable elements will result in the following two ACEs in the output <i>ObjectsSecurityDescriptor</i>:

<ul>
<li>An ACE that is a copy of the original, but with the INHERIT_ONLY flag set</li>
<li>An ACE in which the INHERITED_ACE bit is turned on and the generic elements are mapped to specific elements: 


<ul>
<li>Generic access rights are replaced by the corresponding standard and specific access rights indicated in the input <i>GenericMapping</i>.</li>
<li>Creator Owner SID is replaced with the Owner in the output <i>SecurityDescriptor</i></li>
<li>Creator Group SID is replaced with the Group in the output <i>SecurityDescriptor</i></li>
</ul>
</li>
</ul>
If <i>AutoInheritFlags</i> does not specify the SEF_AVOID_PRIVILEGE_CHECK bit, owner validity checking is performed according to the following rules. The Owner in <i>ModificationDescriptor</i>:

<ul>
<li>Must be a legally formed SID</li>
<li>Must match the TokenUser in <i>Token</i></li>
</ul>
Or

<ul>
<li>Must match a group in the TokenGroups in <i>Token</i> where the attributes on the group: 


<ul>
<li>Include SE_GROUP_OWNER</li>
<li>Include SE_GROUP_USE_FOR_DENY_ONLY</li>
</ul>
</li>
</ul>
A resource manager that is setting the Owner on a subtree of objects can avoid the overhead of redundant owner validity checking. If the Owner in <i>ModificationDescriptor</i> and <i>Token</i> remain the same for iterative calls to this function, the SEF_AVOID_PRIVILEGE_CHECK bit may be set in <i>AutoInheritFlags</i> for calls subsequent to an initial call in which owner validity checking is performed. Callers that do not have access to the token of the client that will ultimately be setting the owner should also choose to skip owner validation checking.

<div class="alert"><b>Note</b>  The SEF_AVOID_PRIVILEGE_CHECK bit as used in the 
<b>SetPrivateObjectSecurityEx</b> function is equivalent to the SEF_AVOID_OWNER_CHECK bit used in the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a> function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity">SetKernelObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity">SetUserObjectSecurity</a>