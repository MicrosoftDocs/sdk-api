---
UID: NF:aclui.ISecurityInformation.GetAccessRights
title: ISecurityInformation::GetAccessRights (aclui.h)
author: windows-sdk-content
description: The GetAccessRights method requests information about the access rights that can be controlled for a securable object.
old-location: security\isecurityinformation_getaccessrights.htm
tech.root: SecAuthZ
ms.assetid: a40b3ded-9a75-476b-bc7e-38794a98261c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAccessRights, GetAccessRights method [Security], GetAccessRights method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetAccessRights method, ISecurityInformation.GetAccessRights, ISecurityInformation::GetAccessRights, SI_ADVANCED, SI_EDIT_AUDITS, SI_EDIT_PROPERTIES, _win32_isecurityinformation_getaccessrights, aclui/ISecurityInformation::GetAccessRights, security.isecurityinformation_getaccessrights
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
 - ISecurityInformation.GetAccessRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::GetAccessRights


## -description


The <b>GetAccessRights</b> method requests information about the access rights that can be controlled for a securable object. The access control editor calls this method to retrieve display strings and other information used to initialize the property pages. For more information, see 
<a href="https://msdn.microsoft.com/da67c486-d2e7-4632-ac7a-c18aabc3f21d">Access Rights and Access Masks</a>.


## -parameters




### -param pguidObjectType [in]

A pointer to a 
<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies the type of object for which access rights are being requested. If this parameter is <b>NULL</b> or a pointer to GUID_NULL, return the access rights for the object being edited. Otherwise, the GUID identifies a child object type returned by the 
<a href="https://msdn.microsoft.com/dafe6c45-616f-4339-a119-9b88055b5d3a">ISecurityInformation::GetInheritTypes</a> method. The GUID corresponds to the <b>InheritedObjectType</b> member of an object-specific ACE.


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
<a href="https://msdn.microsoft.com/9c9b14da-a030-4f90-b090-d6de10507eb2">SI_ACCESS</a> structures. The array must include one entry for each access right. You can specify access rights that apply to the object itself, as well as object-specific access rights that apply only to a property set or property on the object.


### -param pcAccesses [out]

A pointer to <b>ULONG</b> that indicates the number of entries in the <i>ppAccess</i> array.


### -param piDefaultAccess [out]

A pointer to <b>ULONG</b> that indicates the zero-based index of the array entry that contains the default access rights. The access control editor uses this entry as the initial access rights in a new ACE.


## -returns



If the function succeeds, the function returns  S_OK.

 If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>GetAccessRights</b> method is called each time a property page is initialized.

The access control editor does not free the pointer returned in <i>ppAccess</i>.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/dafe6c45-616f-4339-a119-9b88055b5d3a">ISecurityInformation::GetInheritTypes</a>



<a href="https://msdn.microsoft.com/9c9b14da-a030-4f90-b090-d6de10507eb2">SI_ACCESS</a>
 

 

