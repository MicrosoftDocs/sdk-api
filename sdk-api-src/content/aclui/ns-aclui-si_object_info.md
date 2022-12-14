---
UID: NS:aclui._SI_OBJECT_INFO
title: SI_OBJECT_INFO (aclui.h)
description: Used to initialize the access control editor.
helpviewer_keywords: ["*PSI_OBJECT_INFO","PSI_OBJECT_INFO","PSI_OBJECT_INFO structure pointer [Security]","SI_ADVANCED","SI_AUDITS_ELEVATION_REQUIRED","SI_CONTAINER","SI_DISABLE_DENY_ACE","SI_EDIT_ALL","SI_EDIT_AUDITS","SI_EDIT_EFFECTIVE","SI_EDIT_OWNER","SI_EDIT_PERMS","SI_EDIT_PROPERTIES","SI_ENABLE_CENTRAL_POLICY","SI_ENABLE_EDIT_ATTRIBUTE_CONDITION","SI_MAY_WRITE","SI_NO_ACL_PROTECT","SI_NO_ADDITIONAL_PERMISSION","SI_NO_TREE_APPLY","SI_OBJECT_GUID","SI_OBJECT_INFO","SI_OBJECT_INFO structure [Security]","SI_OWNER_ELEVATION_REQUIRED","SI_OWNER_READONLY","SI_OWNER_RECURSE","SI_PAGE_TITLE","SI_PERMS_ELEVATION_REQUIRED","SI_READONLY","SI_RESET","SI_RESET_DACL","SI_RESET_DACL_TREE","SI_RESET_OWNER","SI_RESET_SACL","SI_RESET_SACL_TREE","SI_SCOPE_ELEVATION_REQUIRED","SI_SERVER_IS_DC","SI_VIEW_ONLY","_win32_si_object_info_str","aclui/PSI_OBJECT_INFO","aclui/SI_OBJECT_INFO","security.si_object_info"]
old-location: security\si_object_info.htm
tech.root: security
ms.assetid: bdfd0753-4727-4ca1-ac36-0a77db0a16c5
ms.date: 12/05/2018
ms.keywords: '*PSI_OBJECT_INFO, PSI_OBJECT_INFO, PSI_OBJECT_INFO structure pointer [Security], SI_ADVANCED, SI_AUDITS_ELEVATION_REQUIRED, SI_CONTAINER, SI_DISABLE_DENY_ACE, SI_EDIT_ALL, SI_EDIT_AUDITS, SI_EDIT_EFFECTIVE, SI_EDIT_OWNER, SI_EDIT_PERMS, SI_EDIT_PROPERTIES, SI_ENABLE_CENTRAL_POLICY, SI_ENABLE_EDIT_ATTRIBUTE_CONDITION, SI_MAY_WRITE, SI_NO_ACL_PROTECT, SI_NO_ADDITIONAL_PERMISSION, SI_NO_TREE_APPLY, SI_OBJECT_GUID, SI_OBJECT_INFO, SI_OBJECT_INFO structure [Security], SI_OWNER_ELEVATION_REQUIRED, SI_OWNER_READONLY, SI_OWNER_RECURSE, SI_PAGE_TITLE, SI_PERMS_ELEVATION_REQUIRED, SI_READONLY, SI_RESET, SI_RESET_DACL, SI_RESET_DACL_TREE, SI_RESET_OWNER, SI_RESET_SACL, SI_RESET_SACL_TREE, SI_SCOPE_ELEVATION_REQUIRED, SI_SERVER_IS_DC, SI_VIEW_ONLY, _win32_si_object_info_str, aclui/PSI_OBJECT_INFO, aclui/SI_OBJECT_INFO, security.si_object_info'
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
req.typenames: SI_OBJECT_INFO, *PSI_OBJECT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SI_OBJECT_INFO
 - aclui/_SI_OBJECT_INFO
 - PSI_OBJECT_INFO
 - aclui/PSI_OBJECT_INFO
 - SI_OBJECT_INFO
 - aclui/SI_OBJECT_INFO
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
 - SI_OBJECT_INFO
---

# SI_OBJECT_INFO structure


## -description

The <b>SI_OBJECT_INFO</b> structure is used by the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a> method to specify information used to initialize the access control editor.

## -struct-fields

### -field dwFlags

A set of bit flags that determine the editing options available to the user. This member can be a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SI_ADVANCED_"></a><a id="si_advanced_"></a><dl>
<dt><b>SI_ADVANCED
</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Advanced</b> button is displayed on the basic security property page. If the user clicks this button, the system displays an 
<a href="/windows/desktop/SecAuthZ/advanced-security-property-sheet">advanced security property sheet</a> that enables advanced editing of the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the object. 




Combine this flag with the SI_EDIT_AUDITS, SI_EDIT_OWNER, and SI_EDIT_PROPERTIES flags to enable editing of the object's SACL, owner, and object-specific <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

</td>
</tr>
<tr>
<td width="40%"><a id="SI_AUDITS_ELEVATION_REQUIRED"></a><a id="si_audits_elevation_required"></a><dl>
<dt><b>SI_AUDITS_ELEVATION_REQUIRED</b></dt>
<dt>0x02000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, a shield is displayed on the <b>Edit</b> button of the advanced <b>Auditing</b> pages. For NTFS objects, this flag is requested when the user does not have <b>READ_CONTROL</b> or <b>ACCESS_SYSTEM_SECURITY</b> access.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_CONTAINER_"></a><a id="si_container_"></a><dl>
<dt><b>SI_CONTAINER
</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Indicates that the object is a container. If this flag is set, the access control editor enables the controls relevant to the inheritance of permissions onto child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_DISABLE_DENY_ACE"></a><a id="si_disable_deny_ace"></a><dl>
<dt><b>SI_DISABLE_DENY_ACE</b></dt>
<dt>0x80000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system disables denying an ACE.  Clients of the access control editor must implement the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> interface to set this flag.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_ALL_"></a><a id="si_edit_all_"></a><dl>
<dt><b>SI_EDIT_ALL
</b></dt>
</dl>
</td>
<td width="60%">
Combines the SI_EDIT_PERMS,
SI_EDIT_OWNER, and SI_EDIT_AUDITS flags.
										
								
							

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_AUDITS_"></a><a id="si_edit_audits_"></a><dl>
<dt><b>SI_EDIT_AUDITS
</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
If this flag is set and the user clicks the <b>Advanced</b> button, the system displays an advanced security property sheet that includes an <a href="/windows/desktop/SecAuthZ/auditing-property-page">Auditing property page</a> for editing the object's SACL. To display the <b>Advanced</b> button, set the SI_ADVANCED flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_EFFECTIVE"></a><a id="si_edit_effective"></a><dl>
<dt><b>SI_EDIT_EFFECTIVE</b></dt>
<dt>0x00020000L</dt>
</dl>
</td>
<td width="60%">
 If this flag is set, the <b>Effective Permissions</b> page is displayed. This flag is ignored if the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> object that initialized the access control editor does not implement the <a href="/windows/desktop/api/aclui/nn-aclui-ieffectivepermission">IEffectivePermission</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_OWNER_"></a><a id="si_edit_owner_"></a><dl>
<dt><b>SI_EDIT_OWNER
</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
If this flag is set and the user clicks the <b>Advanced</b> button, the system displays an advanced security property sheet that includes an 
<a href="/windows/desktop/SecAuthZ/owner-property-page">Owner property page</a> for changing the object's owner. To display the <b>Advanced</b> button, set the SI_ADVANCED flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_PERMS_"></a><a id="si_edit_perms_"></a><dl>
<dt><b>SI_EDIT_PERMS
</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
This is the default value. The basic security property page always displays the controls for basic editing of the object's DACL. To disable these controls, set the SI_READONLY flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_PROPERTIES_"></a><a id="si_edit_properties_"></a><dl>
<dt><b>SI_EDIT_PROPERTIES
</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system enables controls for editing ACEs that apply to the object's property sets and properties. These controls are available only on the property sheet displayed when the user clicks the <b>Advanced</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_ENABLE_CENTRAL_POLICY"></a><a id="si_enable_central_policy"></a><dl>
<dt><b>SI_ENABLE_CENTRAL_POLICY</b></dt>
<dt>0x40000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system enables editing attributes.  Clients of the access control editor must implement the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> interface to set this flag.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_ENABLE_EDIT_ATTRIBUTE_CONDITION"></a><a id="si_enable_edit_attribute_condition"></a><dl>
<dt><b>SI_ENABLE_EDIT_ATTRIBUTE_CONDITION</b></dt>
<dt>0x20000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system enables editing attributes.  Clients of the access control editor must implement the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> interface to set this flag.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_MAY_WRITE"></a><a id="si_may_write"></a><dl>
<dt><b>SI_MAY_WRITE</b></dt>
<dt>0x10000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the access control editor cannot read the DACL but might be able to write to the DACL. If a call to the <a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">ISecurityInformation::GetSecurity</a> method returns <b>AccessDenied</b>, the user can try to add a new ACE, and a more appropriate warning is displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_NO_ACL_PROTECT_"></a><a id="si_no_acl_protect_"></a><dl>
<dt><b>SI_NO_ACL_PROTECT
</b></dt>
<dt>0x00000200L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the access control editor hides the check box that allows inheritable ACEs to propagate from the parent object to this object. If this flag is not set, the check box is visible. 




The check box is clear if the SE_DACL_PROTECTED flag is set in the object's security descriptor. In this case, the object's DACL is protected from being modified by inheritable ACEs.

If the user clears the check box, any inherited ACEs in the security descriptor are deleted or converted to noninherited ACEs. Before proceeding with this conversion, the system displays a warning message box to confirm the change.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_NO_ADDITIONAL_PERMISSION"></a><a id="si_no_additional_permission"></a><dl>
<dt><b>SI_NO_ADDITIONAL_PERMISSION</b></dt>
<dt>0x00200000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the access control editor hides the <b>Special Permissions</b> tab on the <b>Advanced Security Settings</b>  page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_NO_TREE_APPLY_"></a><a id="si_no_tree_apply_"></a><dl>
<dt><b>SI_NO_TREE_APPLY
</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the access control editor hides the check box that controls the NO_PROPAGATE_INHERIT_ACE flag. This flag is relevant only when the SI_ADVANCED flag is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_OBJECT_GUID_"></a><a id="si_object_guid_"></a><dl>
<dt><b>SI_OBJECT_GUID
</b></dt>
<dt>0x00010000L</dt>
</dl>
</td>
<td width="60%">
When set, indicates that the <b>guidObjectType</b> member of the <b>SI_OBJECT_INFO</b> structure is valid. This is set in comparisons with object-specific ACEs in determining whether the ACE applies to the current object.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_OWNER_ELEVATION_REQUIRED"></a><a id="si_owner_elevation_required"></a><dl>
<dt><b>SI_OWNER_ELEVATION_REQUIRED</b></dt>
<dt>0x04000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, a shield is displayed on the <b>Edit</b> button of the advanced <b>Owner</b> page. For NTFS objects, this flag is requested when the user does not have <b>WRITE_OWNER</b> access. This flag is valid only if the owner page is requested.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_OWNER_READONLY_"></a><a id="si_owner_readonly_"></a><dl>
<dt><b>SI_OWNER_READONLY
</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the user cannot change the owner of the object. Set this flag if SI_EDIT_OWNER is set but the user does not have permission to change the owner.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_OWNER_RECURSE_"></a><a id="si_owner_recurse_"></a><dl>
<dt><b>SI_OWNER_RECURSE
</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Combine this flag with SI_CONTAINER to display a check box on the owner page that indicates whether the user intends the new owner to be applied to all child objects as well as the current object. The access control editor does not perform the recursion; the recursion should be performed by the application in 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_PAGE_TITLE_"></a><a id="si_page_title_"></a><dl>
<dt><b>SI_PAGE_TITLE
</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>pszPageTitle</b> member is used as the title of the basic security property page. Otherwise, a default title is used.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_PERMS_ELEVATION_REQUIRED"></a><a id="si_perms_elevation_required"></a><dl>
<dt><b>SI_PERMS_ELEVATION_REQUIRED</b></dt>
<dt>0x01000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, an image of a shield is displayed on the <b>Edit</b> button of the simple and advanced <b>Permissions</b> pages. For NTFS objects, this flag is requested when the user does not have <b>READ_CONTROL</b> or <b>WRITE_DAC</b> access.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_READONLY_"></a><a id="si_readonly_"></a><dl>
<dt><b>SI_READONLY
</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the editor displays the object's security information, but the controls for editing the information are disabled.

This flag cannot be combined with the <b>SI_VIEW_ONLY</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_"></a><a id="si_reset_"></a><dl>
<dt><b>SI_RESET
</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Default</b> button is displayed. If the user clicks this button, the access control editor calls the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">ISecurityInformation::GetSecurity</a> method to retrieve an application-defined default security descriptor. The access control editor uses this security descriptor to reinitialize the property sheet, and the user is allowed to apply the change or cancel.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_DACL"></a><a id="si_reset_dacl"></a><dl>
<dt><b>SI_RESET_DACL</b></dt>
<dt>0x00040000L</dt>
</dl>
</td>
<td width="60%">
When set, this flag displays the <b>Reset Defaults</b> button on the <b>Permissions</b> page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_DACL_TREE_"></a><a id="si_reset_dacl_tree_"></a><dl>
<dt><b>SI_RESET_DACL_TREE
</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">
When set, this flag displays the Reset permissions on all child objects and enable propagation of inheritable permissions check box in the Permissions page of the Access Control Settings window. If this check box is selected when the user clicks the <b>Apply</b> button, a bitwise-<b>OR</b> operation is performed on the <i>SecurityInformation</i> parameter of 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a> with SI_RESET_DACL_TREE. This function does not reset the permissions and enable propagation of inheritable permissions; the implementation of <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> must do this.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_OWNER"></a><a id="si_reset_owner"></a><dl>
<dt><b>SI_RESET_OWNER</b></dt>
<dt>0x00100000L</dt>
</dl>
</td>
<td width="60%">
When set, this flag displays the <b>Reset Defaults</b> button on the <b>Owner</b> page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_SACL"></a><a id="si_reset_sacl"></a><dl>
<dt><b>SI_RESET_SACL</b></dt>
<dt>0x00080000L</dt>
</dl>
</td>
<td width="60%">
When set, this flag displays the <b>Reset Defaults</b> button on the <b>Auditing</b> page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_RESET_SACL_TREE_"></a><a id="si_reset_sacl_tree_"></a><dl>
<dt><b>SI_RESET_SACL_TREE
</b></dt>
<dt>0x00008000L</dt>
</dl>
</td>
<td width="60%">
When set, this flag displays the Reset auditing entries on all child objects and enables propagation of the inheritable auditing entries check box in the Auditing page of the Access Control Settings window. If this check box is selected when the user clicks the <b>Apply</b> button, a bitwise-<b>OR</b> operation is performed on the <i>SecurityInformation</i> parameter of 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a> with SI_RESET_SACL_TREE. This function does not reset the permissions and enable propagation of inheritable permissions; the implementation of <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a> must do this.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_SCOPE_ELEVATION_REQUIRED"></a><a id="si_scope_elevation_required"></a><dl>
<dt><b>SI_SCOPE_ELEVATION_REQUIRED</b></dt>
<dt>0x08000000L</dt>
</dl>
</td>
<td width="60%">
If this flag is set, an image of a shield is displayed on the <b>Change</b> button of the Scope attribute. For NTFS objects, this flag is requested when the user does not have READ_CONTROL or WRITE_DAC access.  Clients of the access control editor must implement the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation4">ISecurityInformation4</a> interface to set this flag.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_SERVER_IS_DC_"></a><a id="si_server_is_dc_"></a><dl>
<dt><b>SI_SERVER_IS_DC
</b></dt>
<dt>0x00001000L</dt>
</dl>
</td>
<td width="60%">
Set this flag if the <b>pszServerName</b> computer is known to be a domain controller. If this flag is set, the domain name is included in the scope list of the <b>Add Users and Groups</b> dialog box. Otherwise, the <b>pszServerName</b> computer is used to determine the scope list of the dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_VIEW_ONLY"></a><a id="si_view_only"></a><dl>
<dt><b>SI_VIEW_ONLY</b></dt>
<dt>0x00400000L</dt>
</dl>
</td>
<td width="60%">
This flag is set by the access control editor client to display read-only versions of the access control editor dialog boxes. These versions of the dialog boxes do not allow editing of the associated object's permissions. Clients of the access control editor must implement the <a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation3">ISecurityInformation3</a> interface to set this flag.

This flag cannot be combined with the <b>SI_READONLY</b> flag.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
</table>

### -field hInstance

Identifies a module that contains string resources to be used in the property sheet. The 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getaccessrights">ISecurityInformation::GetAccessRights</a> and 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getinherittypes">ISecurityInformation::GetInheritTypes</a> methods can specify string resource identifiers for display names.

### -field pszServerName

A pointer to a <b>null</b>-terminated, <a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string that names the computer on which to look up account names and SIDs. This value can be <b>NULL</b> to specify the local computer. The access control editor does not free this pointer.

### -field pszObjectName

A pointer to a <b>null</b>-terminated, Unicode string that names the object being edited. This name appears in the title of the advanced security property sheet and any error message boxes displayed by the access control editor. The access control editor does not free this pointer.

### -field pszPageTitle

A pointer to a <b>null</b>-terminated, Unicode string used as the title of the basic security property page. This member is ignored unless the SI_PAGE_TITLE flag is set in <b>dwFlags</b>. If the page title is not provided, a default title is used. The access control editor does not free this pointer.

### -field guidObjectType

A 
GUID for the object. This member is ignored unless the SI_OBJECT_GUID flag is set in <b>dwFlags</b>.

## -see-also

<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getaccessrights">ISecurityInformation::GetAccessRights</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getinherittypes">ISecurityInformation::GetInheritTypes</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getsecurity">ISecurityInformation::GetSecurity</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-setsecurity">ISecurityInformation::SetSecurity</a>