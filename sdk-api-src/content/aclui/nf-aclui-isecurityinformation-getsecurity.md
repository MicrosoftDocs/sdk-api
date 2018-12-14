---
UID: NF:aclui.ISecurityInformation.GetSecurity
title: ISecurityInformation::GetSecurity
author: windows-sdk-content
description: The GetSecurity method requests a security descriptor for the securable object whose security descriptor is being edited. The access control editor calls this method to retrieve the object's current or default security descriptor.
old-location: security\isecurityinformation_getsecurity.htm
tech.root: secauthz
ms.assetid: 4c9e05fd-0b58-4d6d-b33e-067d9e8e2915
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, GetSecurity, GetSecurity method [Security], GetSecurity method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetSecurity method, ISecurityInformation.GetSecurity, ISecurityInformation::GetSecurity, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, _win32_isecurityinformation_getsecurity, aclui/ISecurityInformation::GetSecurity, security.isecurityinformation_getsecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.GetSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::GetSecurity


## -description


The <b>GetSecurity</b> method requests a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for the securable object whose security descriptor is being edited. The access control editor calls this method to retrieve the object's current or default security descriptor.


## -parameters




### -param RequestedInformation [in]

A set of 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags that indicate the parts of the security descriptor being requested. This parameter can be a combination of the following values.

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
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free the returned pointer.


### -param fDefault [in]

If this parameter is <b>TRUE</b>, <i>ppSecurityDescriptor</i> should return an application-defined default security descriptor for the object. The access control editor uses this default security descriptor to reinitialize the property page. 




The access control editor sets this parameter to <b>TRUE</b> only if the user clicks the <b>Default</b> button. The <b>Default</b> button is displayed only if you set the SI_RESET flag in the 
<a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">ISecurityInformation::GetObjectInformation</a> method. If no default security descriptor is available, do not set the SI_RESET flag.

If this flag is <b>FALSE</b>, <i>ppSecurityDescriptor</i> should return the object's current security descriptor.


## -returns



Returns S_OK if successful.

Returns a nonzero error code if an error occurs. Returns E_ACCESSDENIED if the user does not have permission to read the requested security information.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">ISecurityInformation::GetObjectInformation</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>
 

 

