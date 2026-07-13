---
UID: NF:securitybaseapi.CreatePrivateObjectSecurityWithMultipleInheritance
title: CreatePrivateObjectSecurityWithMultipleInheritance function (securitybaseapi.h)
description: Allocates and initializes a self-relative security descriptor for a new private object created by the resource manager calling this function. (CreatePrivateObjectSecurityWithMultipleInheritance)
helpviewer_keywords: ["CreatePrivateObjectSecurityWithMultipleInheritance","CreatePrivateObjectSecurityWithMultipleInheritance function [Security]","SEF_AVOID_OWNER_CHECK","SEF_AVOID_OWNER_RESTRICTION","SEF_AVOID_PRIVILEGE_CHECK","SEF_DACL_AUTO_INHERIT","SEF_DEFAULT_DESCRIPTOR_FOR_OBJECT","SEF_DEFAULT_GROUP_FROM_PARENT","SEF_DEFAULT_OWNER_FROM_PARENT","SEF_MACL_NO_EXECUTE_UP","SEF_MACL_NO_READ_UP","SEF_MACL_NO_WRITE_UP","SEF_SACL_AUTO_INHERIT","_win32_createprivateobjectsecuritywithmultipleinheritance","security.createprivateobjectsecuritywithmultipleinheritance","securitybaseapi/CreatePrivateObjectSecurityWithMultipleInheritance"]
old-location: security\createprivateobjectsecuritywithmultipleinheritance.htm
tech.root: security
ms.assetid: 8c5a2ac2-612c-4625-8c68-27d99d4ba9d5
ms.date: 12/05/2018
ms.keywords: CreatePrivateObjectSecurityWithMultipleInheritance, CreatePrivateObjectSecurityWithMultipleInheritance function [Security], SEF_AVOID_OWNER_CHECK, SEF_AVOID_OWNER_RESTRICTION, SEF_AVOID_PRIVILEGE_CHECK, SEF_DACL_AUTO_INHERIT, SEF_DEFAULT_DESCRIPTOR_FOR_OBJECT, SEF_DEFAULT_GROUP_FROM_PARENT, SEF_DEFAULT_OWNER_FROM_PARENT, SEF_MACL_NO_EXECUTE_UP, SEF_MACL_NO_READ_UP, SEF_MACL_NO_WRITE_UP, SEF_SACL_AUTO_INHERIT, _win32_createprivateobjectsecuritywithmultipleinheritance, security.createprivateobjectsecuritywithmultipleinheritance, securitybaseapi/CreatePrivateObjectSecurityWithMultipleInheritance
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
 - CreatePrivateObjectSecurityWithMultipleInheritance
 - securitybaseapi/CreatePrivateObjectSecurityWithMultipleInheritance
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
 - CreatePrivateObjectSecurityWithMultipleInheritance
---

# CreatePrivateObjectSecurityWithMultipleInheritance function


## -description

The <b>CreatePrivateObjectSecurityWithMultipleInheritance</b> function allocates and initializes a <a href="/windows/desktop/SecGloss/s-gly">self-relative security descriptor</a> for a new private object created by the resource manager calling this function. This function supports private objects (such as Directory Service objects with attached auxiliary classes) composed of multiple object types or classes.

## -parameters

### -param ParentDescriptor [in, optional]

A pointer to the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the parent container of the object. If there is no parent container, this parameter is <b>NULL</b>.

### -param CreatorDescriptor [in, optional]

A pointer to a security descriptor provided by the creator of the object. If the object's creator does not explicitly pass security information for the new object, this parameter can be <b>NULL</b>. Alternatively, this parameter can point to a default security descriptor.

### -param NewDescriptor [out]

A pointer to a variable to receive a pointer to the newly allocated self-relative security descriptor. When you have finished using the security descriptor, free it by calling the  
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a> function.

### -param ObjectTypes [in, optional]

An array of pointers to <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structures that identify the object types or classes of the object associated with <i>NewDescriptor</i>. For Active Directory objects, this array contains pointers to the class GUIDs of the object's structural class and all attached auxiliary classes. Set <i>ObjectTypes</i> to <b>NULL</b> if the object does not have a GUID.

### -param GuidCount [in]

The number of GUIDs present in the <i>ObjectTypes</i> parameter.

### -param IsContainerObject [in]

Specifies whether the new object can contain other objects. A value of <b>TRUE</b> indicates that the new object is a container. A value of <b>FALSE</b> indicates that the new object is not a container.

### -param AutoInheritFlags [in]

A set of bit flags that control how <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) are inherited from <i>ParentDescriptor</i>. This parameter can be a combination of the following values.

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
        <i>ParentDescriptor</i>, as well as any explicit ACEs specified in the DACL of 
        <i>CreatorDescriptor</i>. If this flag is not set, the new DACL does not inherit ACEs.

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
        <i>ParentDescriptor</i>, as well as any explicit ACEs specified in the SACL of 
        <i>CreatorDescriptor</i>. If this flag is not set, the new SACL does not inherit ACEs.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_DEFAULT_DESCRIPTOR_FOR_OBJECT"></a><a id="sef_default_descriptor_for_object"></a><dl>
<dt><b>SEF_DEFAULT_DESCRIPTOR_FOR_OBJECT</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
<i>CreatorDescriptor</i> is the default descriptor for the types of objects specified by <i>ObjectTypes</i>. As such, 
        <i>CreatorDescriptor</i> is ignored if 
        <i>ParentDescriptor</i> has any object-specific ACEs for the types of objects specified by the <i>ObjectTypes</i> parameter. If no such ACEs are inherited, 
        <i>CreatorDescriptor</i> is handled as though this flag were not specified.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_AVOID_PRIVILEGE_CHECK"></a><a id="sef_avoid_privilege_check"></a><dl>
<dt><b>SEF_AVOID_PRIVILEGE_CHECK</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The function does not perform privilege checking. If the SEF_AVOID_OWNER_CHECK flag is also set, the <i>Token</i> parameter can be <b>NULL</b>. This flag is useful while implementing automatic inheritance to avoid checking privileges on each child updated.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_AVOID_OWNER_CHECK"></a><a id="sef_avoid_owner_check"></a><dl>
<dt><b>SEF_AVOID_OWNER_CHECK</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The function does not check the validity of the owner in the resultant <i>NewDescriptor</i> as described in the Remarks section. If the SEF_AVOID_PRIVILEGE_CHECK flag is also set, the <i>Token</i> parameter can be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_DEFAULT_OWNER_FROM_PARENT"></a><a id="sef_default_owner_from_parent"></a><dl>
<dt><b>SEF_DEFAULT_OWNER_FROM_PARENT</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
The owner of <i>NewDescriptor</i> defaults to the owner from <i>ParentDescriptor</i>. If not set, the owner of <i>NewDescriptor</i> defaults to the owner of the token specified by the <i>Token</i> parameter. The owner of the token is specified in the token itself. In either case, if the <i>CreatorDescriptor</i> parameter is not <b>NULL</b>, the <i>NewDescriptor</i> owner is set to the owner from <i>CreatorDescriptor</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEF_DEFAULT_GROUP_FROM_PARENT"></a><a id="sef_default_group_from_parent"></a><dl>
<dt><b>SEF_DEFAULT_GROUP_FROM_PARENT</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
The group of <i>NewDescriptor</i> defaults to the group from <i>ParentDescriptor</i>. If not set, the group of <i>NewDescriptor</i> defaults to the group of the token specified by the <i>Token</i> parameter. The group of the token is specified in the token itself. In either case, if the <i>CreatorDescriptor</i> parameter is not <b>NULL</b>, the <i>NewDescriptor</i> group is set to the group from <i>CreatorDescriptor</i>.

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
            <i>ParentDescriptor</i> parameter that would limit the caller's ability to specify
            a DACL in the <i>CreatorDescriptor</i> are ignored.

</td>
</tr>
</table>

### -param Token [in, optional]

A handle to the <a href="/windows/desktop/SecGloss/a-gly">access token</a> for the client <a href="/windows/desktop/SecGloss/p-gly">process</a> on whose behalf the object is being created. If this is an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, it must be at SecurityIdentification level or higher. For a full description of the SecurityIdentification impersonation level, see the 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumerated type. 




The client token contains default security information, such as the default owner, primary group, and DACL. This function uses these defaults if the information is not in the input security descriptors. The token must be open for <b>TOKEN_QUERY</b> access.

If all of the following conditions are true, then the handle must be opened for <b>TOKEN_DUPLICATE</b> access in addition to <b>TOKEN_QUERY</b> access.

<ul>
<li>The token handle refers to a primary token.</li>
<li>The security descriptor of the token contains one or more ACEs with the <b>OwnerRights</b> SID.</li>
<li>A security descriptor is specified for the <i>CreatorDescriptor</i> parameter.</li>
<li>The caller of this function does not set the <b>SEF_AVOID_OWNER_RESTRICTION</b> flag in the <i>AutoInheritFlags</i> parameter.</li>
</ul>

### -param GenericMapping [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a> structure that specifies the mapping from each generic right to specific rights for the object.

## -returns

If the function succeeds, the function returns a nonzero value. 

If the function fails, it returns zero. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information. Some extended error codes and their meanings are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PRIMARY_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The function cannot retrieve a primary group for the new security descriptor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OWNER</b></dt>
</dl>
</td>
<td width="60%">
The function cannot retrieve an owner for the new security descriptor or the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) cannot be assigned as an owner. This occurs when validating the owner SID against the passed-in token.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The function received <b>NULL</b> instead of a token for owner validation or <a href="/windows/desktop/SecGloss/p-gly">privilege</a> checking.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
A SACL is being set, SEF_AVOID_PRIVILEGE_CHECK was not passed in, and the token passed in did not have SE_SECURITY_NAME enabled.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a> function is identical to calling the 
<b>CreatePrivateObjectSecurityWithMultipleInheritance</b> function with a single GUID in <i>ObjectTypes</i>.

The <i>AutoInheritFlags</i> are distinct from the similarly named bits in the <b>Control</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. For an explanation of the control bits, see 
<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>.

If <i>AutoInheritFlags</i> specifies the SEF_DACL_AUTO_INHERIT bit, the function applies the following rules to the DACL in the new security descriptor:

<ul>
<li>The SE_DACL_AUTO_INHERITED flag is set in the <b>Control</b> member of the new security descriptor.</li>
<li>The DACL of the new security descriptor inherits ACEs from <i>ParentDescriptor</i> regardless of whether <i>CreatorDescriptor</i> is the default security descriptor or was explicitly specified by the creator. The new DACL is a combination of the parent and creator DACLs as defined by the rules of inheritance. Specifically, any ACEs in <i>ParentDescriptor</i> that are inheritable either to all child objects or to any object class listed in <i>ObjectTypes</i> will be applied to the new DACL.</li>
<li>Inherited ACEs are marked as INHERITED_ACE.</li>
</ul>
If <i>AutoInheritFlags</i> specifies the SEF_SACL_AUTO_INHERIT bit, the function applies similar rules to the new SACL.

For both DACLs and SACLs, certain types of ACEs in <i>ParentDescriptor</i> and <i>CreatorDescriptor</i> will be manipulated and possibly replaced by two ACEs in <i>NewDescriptor</i>. Specifically, an inheritable ACE that contains at least one of the following mappable elements may result in two ACEs in the output security descriptor. Mappable elements include:

<ul>
<li>Generic access rights in the ACCESS_MASK</li>
<li>Creator Owner SID or Creator Group SID as the ACE subject identifier</li>
</ul>
ACEs with any of these mappable elements will result in the following two ACEs in <i>NewDescriptor</i>:

<ul>
<li>An ACE that is a copy of the original, but with the INHERIT_ONLY flag set. However, this ACE will not be created if either of the following two conditions exist: 


<ul>
<li>The <i>IsContainerObject</i> parameter is <b>FALSE</b>. Inheritable ACEs are meaningless on noncontainer objects.</li>
<li>The original ACE contains the NO_PROPAGATE_INHERIT flag. The original ACE is intended to be inherited as an effective ACE on children, but not inheritable below those children.</li>
</ul>
</li>
<li>An effective ACE in which the INHERITED_ACE bit is turned on and the generic elements are mapped to specific elements: 


<ul>
<li>Generic access rights are replaced by the corresponding standard and specific access rights indicated in the input <i>GenericMapping</i>.</li>
<li>Creator Owner SID is replaced with the Owner in the resultant <i>NewDescriptor</i></li>
<li>Creator Group SID is replaced with the Group in the resultant <i>NewDescriptor</i></li>
</ul>
</li>
</ul>
If <i>AutoInheritFlags</i> does not specify the SEF_AVOID_OWNER_CHECK bit, owner validity checking is performed according to the following rules. The Owner in the resultant <i>NewDescriptor</i> must be a legally formed SID, and either must match the TokenUser in <i>Token</i> or must match a group in the TokenGroups in <i>Token</i>. The attributes on the group:

<ul>
<li>Must include SE_GROUP_OWNER</li>
<li>Must not include SE_GROUP_USE_FOR_DENY_ONLY</li>
</ul>
Callers that do not have access to the token of the client that will ultimately be setting the owner may choose to skip owner validation checking.

To create a security descriptor for a new object, call <b>CreatePrivateObjectSecurityWithMultipleInheritance</b> with <i>ParentDescriptor</i> set to the security descriptor of the parent container and <i>CreatorDescriptor</i> set to the security descriptor proposed by the creator of the object.

To verify the current security descriptor on an object, call <b>CreatePrivateObjectSecurityWithMultipleInheritance</b> with <i>ParentDescriptor</i> set to the security descriptor of the parent container and <i>CreatorDescriptor</i> set to the current security descriptor of the object. This call ensures that the ACEs are appropriately inherited from parent to child security descriptors.

If the <i>CreatorDescriptor</i> security descriptor contains a SACL, <i>Token</i> must have the SE_SECURITY_NAME privilege enabled or the caller must specify the SEF_AVOID_PRIVILEGE_CHECK flag in <i>AutoInheritFlags</i>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurityex">CreatePrivateObjectSecurityEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity">DestroyPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-generic_mapping">GENERIC_MAPPING</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-control">SECURITY_DESCRIPTOR_CONTROL</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>
