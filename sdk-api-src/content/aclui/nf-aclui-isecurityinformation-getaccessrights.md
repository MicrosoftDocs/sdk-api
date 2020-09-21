---
UID: NF:aclui.ISecurityInformation.GetAccessRights
title: ISecurityInformation::GetAccessRights (aclui.h)
description: The GetAccessRights method requests information about the access rights that can be controlled for a securable object.
helpviewer_keywords: ["GetAccessRights","GetAccessRights method [Security]","GetAccessRights method [Security]","ISecurityInformation interface","ISecurityInformation interface [Security]","GetAccessRights method","ISecurityInformation.GetAccessRights","ISecurityInformation::GetAccessRights","SI_ADVANCED","SI_EDIT_AUDITS","SI_EDIT_PROPERTIES","_win32_isecurityinformation_getaccessrights","aclui/ISecurityInformation::GetAccessRights","security.isecurityinformation_getaccessrights"]
old-location: security\isecurityinformation_getaccessrights.htm
tech.root: security
ms.assetid: a40b3ded-9a75-476b-bc7e-38794a98261c
ms.date: 12/05/2018
ms.keywords: GetAccessRights, GetAccessRights method [Security], GetAccessRights method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetAccessRights method, ISecurityInformation.GetAccessRights, ISecurityInformation::GetAccessRights, SI_ADVANCED, SI_EDIT_AUDITS, SI_EDIT_PROPERTIES, _win32_isecurityinformation_getaccessrights, aclui/ISecurityInformation::GetAccessRights, security.isecurityinformation_getaccessrights
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISecurityInformation::GetAccessRights
 - aclui/ISecurityInformation::GetAccessRights
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.GetAccessRights
---

# ISecurityInformation::GetAccessRights


## -description

The <b>GetAccessRights</b> method requests information about the access rights that can be controlled for a securable object. The access control editor calls this method to retrieve display strings and other information used to initialize the property pages. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">Access Rights and Access Masks</a>.

## -parameters

### -param pguidObjectType [in]

A pointer to a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object for which access rights are being requested. If this parameter is <b>NULL</b> or a pointer to GUID_NULL, return the access rights for the object being edited. Otherwise, the GUID identifies a child object type returned by the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getinherittypes">ISecurityInformation::GetInheritTypes</a> method. The GUID corresponds to the <b>InheritedObjectType</b> member of an object-specific ACE.

### -param dwFlags [in]

A set of bit flags that indicate the property page being initialized. This value is zero if the basic security page is being initialized. Otherwise, it is a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SI_ADVANCED"></a><a id="si_advanced"></a><dl>
<dt><b>SI_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
The <b>Advanced Security</b> property sheet is being initialized.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_AUDITS"></a><a id="si_edit_audits"></a><dl>
<dt><b>SI_EDIT_AUDITS</b></dt>
</dl>
</td>
<td width="60%">
The <b>Advanced Security</b> property sheet includes the <b>Audit</b> property page.

</td>
</tr>
<tr>
<td width="40%"><a id="SI_EDIT_PROPERTIES"></a><a id="si_edit_properties"></a><dl>
<dt><b>SI_EDIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The <b>Advanced Security</b> property sheet enables editing of ACEs that apply to the properties and property sets of the object.

</td>
</tr>
</table>

### -param ppAccess [out]

A pointer to an array of 
<a href="/windows/desktop/api/aclui/ns-aclui-si_access">SI_ACCESS</a> structures. The array must include one entry for each access right. You can specify access rights that apply to the object itself, as well as object-specific access rights that apply only to a property set or property on the object.

### -param pcAccesses [out]

A pointer to <b>ULONG</b> that indicates the number of entries in the <i>ppAccess</i> array.

### -param piDefaultAccess [out]

A pointer to <b>ULONG</b> that indicates the zero-based index of the array entry that contains the default access rights. The access control editor uses this entry as the initial access rights in a new ACE.

## -returns

If the function succeeds, the function returns  S_OK.

 If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>GetAccessRights</b> method is called each time a property page is initialized.

The access control editor does not free the pointer returned in <i>ppAccess</i>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nf-aclui-createsecuritypage">CreateSecurityPage</a>



<a href="/windows/desktop/api/aclui/nf-aclui-editsecurity">EditSecurity</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getinherittypes">ISecurityInformation::GetInheritTypes</a>



<a href="/windows/desktop/api/aclui/ns-aclui-si_access">SI_ACCESS</a>