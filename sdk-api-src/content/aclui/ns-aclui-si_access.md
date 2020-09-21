---
UID: NS:aclui._SI_ACCESS
title: SI_ACCESS (aclui.h)
description: Contains information about an access right or default access mask for a securable object.
helpviewer_keywords: ["*PSI_ACCESS","CONTAINER_INHERIT_ACE","INHERIT_ONLY_ACE","OBJECT_INHERIT_ACE","PSI_ACCESS","PSI_ACCESS structure pointer [Security]","SI_ACCESS","SI_ACCESS structure [Security]","SI_ACCESS_CONTAINER","SI_ACCESS_GENERAL","SI_ACCESS_PROPERTY","SI_ACCESS_SPECIFIC","_win32_si_access_str","aclui/PSI_ACCESS","aclui/SI_ACCESS","security.si_access"]
old-location: security\si_access.htm
tech.root: security
ms.assetid: 9c9b14da-a030-4f90-b090-d6de10507eb2
ms.date: 12/05/2018
ms.keywords: '*PSI_ACCESS, CONTAINER_INHERIT_ACE, INHERIT_ONLY_ACE, OBJECT_INHERIT_ACE, PSI_ACCESS, PSI_ACCESS structure pointer [Security], SI_ACCESS, SI_ACCESS structure [Security], SI_ACCESS_CONTAINER, SI_ACCESS_GENERAL, SI_ACCESS_PROPERTY, SI_ACCESS_SPECIFIC, _win32_si_access_str, aclui/PSI_ACCESS, aclui/SI_ACCESS, security.si_access'
req.header: aclui.h
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
req.typenames: SI_ACCESS, *PSI_ACCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SI_ACCESS
 - aclui/_SI_ACCESS
 - PSI_ACCESS
 - aclui/PSI_ACCESS
 - SI_ACCESS
 - aclui/SI_ACCESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - SI_ACCESS
---

# SI_ACCESS structure


## -description

The <b>SI_ACCESS</b> structure contains information about an access right or default <a href="/windows/desktop/SecGloss/a-gly">access mask</a> for a securable object. The 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getaccessrights">ISecurityInformation::GetAccessRights</a> method uses this structure to specify information that the access control editor uses to initialize its property pages.

## -struct-fields

### -field pguid

A pointer to a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object to which the access right or default access mask applies. The GUID can identify a property set or property on the object, or a type of child object that can be contained by the object. 




If this member points to GUID_NULL, the access right applies to the object itself.

### -field mask

A bitmask that specifies the access right described by this structure. The mask can contain any combination of standard and specific rights, but should not contain generic rights such as GENERIC_ALL.

### -field pszName

A pointer to a null-terminated <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string containing a display string that describes the access right. 




Alternatively, <b>pszName</b> can be a string resource identifier returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. Use the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a> method to identify the module that contains the string resource.

### -field dwFlags

A set of bit flags that indicate where the access right is displayed. This member can be a combination of the following. 




						
						
					



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SI_ACCESS_SPECIFIC"></a><a id="si_access_specific"></a><dl>
<dt><b>SI_ACCESS_SPECIFIC</b></dt>
</dl>
</td>
<td width="60%">
The access right is displayed on the advanced security pages.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_ACCESS_GENERAL"></a><a id="si_access_general"></a><dl>
<dt><b>SI_ACCESS_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
The access right is displayed on the basic security page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_ACCESS_CONTAINER"></a><a id="si_access_container"></a><dl>
<dt><b>SI_ACCESS_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
Indicates an access right that applies only to containers. If this flag is set, the access right is displayed on the basic security page only if the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a> method specifies the SI_CONTAINER flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_ACCESS_PROPERTY"></a><a id="si_access_property"></a><dl>
<dt><b>SI_ACCESS_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
Indicates a property-specific access right. Used with SI_EDIT_PROPERTIES.

</td>
</tr>
</table>
 


This member can also specify a combination of the following flags to indicate whether other containers or objects can inherit the access right.



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
Other containers that are contained by the primary object inherit the entry.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the primary object to which the ACL is attached, but objects contained by the primary object inherit the entry.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the entry.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getaccessrights">ISecurityInformation::GetAccessRights</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a>