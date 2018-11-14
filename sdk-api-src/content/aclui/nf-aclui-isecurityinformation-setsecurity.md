---
UID: NF:aclui.ISecurityInformation.SetSecurity
title: ISecurityInformation::SetSecurity
author: windows-sdk-content
description: The SetSecurity method provides a security descriptor containing the security information the user wants to apply to the securable object. The access control editor calls this method when the user clicks Okay or Apply.
old-location: security\isecurityinformation_setsecurity.htm
tech.root: secauthz
ms.assetid: 7c23c5ad-8088-4cfb-9746-99d24cc3bd0e
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, ISecurityInformation interface [Security],SetSecurity method, ISecurityInformation.SetSecurity, ISecurityInformation::SetSecurity, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetSecurity, SetSecurity method [Security], SetSecurity method [Security],ISecurityInformation interface, _win32_isecurityinformation_setsecurity, aclui/ISecurityInformation::SetSecurity, security.isecurityinformation_setsecurity
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
 - ISecurityInformation.SetSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- aclui.h
: 
- ISecurityInformation.SetSecurity
: 
---

# ISecurityInformation::SetSecurity


## -description


The <b>SetSecurity</b> method provides a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> containing the security information the user wants to apply to the securable object. The access control editor calls this method when the user clicks <b>Okay</b> or <b>Apply</b>.


## -parameters




### -param SecurityInformation [in]

A set of 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags that indicate the parts of the security descriptor to set. This parameter can be a combination of the following values. 




					

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
The security descriptor contains the SID of the object's owner.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor contains the SID of the object's primary group.

</td>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor contains the object's DACL.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The security descriptor contains the object's SACL.

</td>
</tr>
</table>
 


### -param pSecurityDescriptor [in]

A pointer to a security descriptor containing the new security information. Do not assume the security descriptor is in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> form; it  can be either 
<a href="https://msdn.microsoft.com/dab2844b-7df9-446c-aacf-380a0a805cbc">absolute or self-relative</a>.


## -returns



Returns S_OK if successful.

Returns a nonzero error code if an error occurs.




## -remarks



To build a complete security descriptor for the object, the application must merge the new security descriptor parts, as defined by the <i>SecurityInformation</i> parameter, into the object's existing security descriptor.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>
 

 

