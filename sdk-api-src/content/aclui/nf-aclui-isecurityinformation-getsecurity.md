---
UID: NF:aclui.ISecurityInformation.GetSecurity
title: ISecurityInformation::GetSecurity (aclui.h)
description: The GetSecurity method requests a security descriptor for the securable object whose security descriptor is being edited. The access control editor calls this method to retrieve the object's current or default security descriptor.
helpviewer_keywords: ["DACL_SECURITY_INFORMATION","GROUP_SECURITY_INFORMATION","GetSecurity","GetSecurity method [Security]","GetSecurity method [Security]","ISecurityInformation interface","ISecurityInformation interface [Security]","GetSecurity method","ISecurityInformation.GetSecurity","ISecurityInformation::GetSecurity","OWNER_SECURITY_INFORMATION","SACL_SECURITY_INFORMATION","_win32_isecurityinformation_getsecurity","aclui/ISecurityInformation::GetSecurity","security.isecurityinformation_getsecurity"]
old-location: security\isecurityinformation_getsecurity.htm
tech.root: security
ms.assetid: 4c9e05fd-0b58-4d6d-b33e-067d9e8e2915
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, GetSecurity, GetSecurity method [Security], GetSecurity method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetSecurity method, ISecurityInformation.GetSecurity, ISecurityInformation::GetSecurity, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, _win32_isecurityinformation_getsecurity, aclui/ISecurityInformation::GetSecurity, security.isecurityinformation_getsecurity
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
 - ISecurityInformation::GetSecurity
 - aclui/ISecurityInformation::GetSecurity
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
 - ISecurityInformation.GetSecurity
---

# ISecurityInformation::GetSecurity


## -description

The <b>GetSecurity</b> method requests a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the securable object whose security descriptor is being edited. The access control editor calls this method to retrieve the object's current or default security descriptor.

## -parameters

### -param RequestedInformation [in]

A set of 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> bit flags that indicate the parts of the security descriptor being requested. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OWNER_SECURITY_INFORMATION"></a><a id="owner_security_information"></a><dl>
<dt><b>OWNER_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor must include the SID of the object's owner.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor must include the SID of the object's primary group.

</td>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor must include the object's DACL.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor must include the object's SACL.

</td>
</tr>
</table>

### -param ppSecurityDescriptor [out]

A pointer to a variable that your implementation must set to a pointer to the object's security descriptor. The security descriptor must include the components requested by the <i>RequestedInformation</i> parameter. 




The system calls the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free the returned pointer.

### -param fDefault [in]

If this parameter is <b>TRUE</b>, <i>ppSecurityDescriptor</i> should return an application-defined default security descriptor for the object. The access control editor uses this default security descriptor to reinitialize the property page. 




The access control editor sets this parameter to <b>TRUE</b> only if the user clicks the <b>Default</b> button. The <b>Default</b> button is displayed only if you set the SI_RESET flag in the 
<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a> method. If no default security descriptor is available, do not set the SI_RESET flag.

If this flag is <b>FALSE</b>, <i>ppSecurityDescriptor</i> should return the object's current security descriptor.

## -returns

Returns S_OK if successful.

Returns a nonzero error code if an error occurs. Returns E_ACCESSDENIED if the user does not have permission to read the requested security information.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control-editor">Access Control Editor</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Access Control Editor Functions</a>



<a href="/windows/desktop/api/aclui/nn-aclui-isecurityinformation">ISecurityInformation</a>



<a href="/windows/desktop/api/aclui/nf-aclui-isecurityinformation-getobjectinformation">ISecurityInformation::GetObjectInformation</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>