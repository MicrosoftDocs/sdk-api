---
UID: NS:aclui._SI_INHERIT_TYPE
title: "_SI_INHERIT_TYPE"
author: windows-sdk-content
description: Contains information about how access control entries (ACEs) can be inherited by child objects.
old-location: security\si_inherit_type.htm
old-project: secauthz
ms.assetid: e8382c14-d3b4-4a7e-aeaa-06ef44d6ace2
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: "*PSI_INHERIT_TYPE, CONTAINER_INHERIT_ACE, INHERIT_ONLY_ACE, OBJECT_INHERIT_ACE, PSI_INHERIT_TYPE, PSI_INHERIT_TYPE structure pointer [Security], SI_INHERIT_TYPE, SI_INHERIT_TYPE structure [Security], _SI_INHERIT_TYPE, _win32_si_inherit_type_str, aclui/PSI_INHERIT_TYPE, aclui/SI_INHERIT_TYPE, security.si_inherit_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SI_INHERIT_TYPE, *PSI_INHERIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - SI_INHERIT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _SI_INHERIT_TYPE structure


## -description


The <b>SI_INHERIT_TYPE</b> structure contains information about how <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) can be inherited by child objects. The 
<a href="https://msdn.microsoft.com/dafe6c45-616f-4339-a119-9b88055b5d3a">ISecurityInformation::GetInheritTypes</a> method uses this structure to specify display strings that the access control editor uses to initialize its property pages.


## -struct-fields




### -field pguid

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies the type of child object. This member can be a pointer to GUID_NULL. The GUID corresponds to the <b>InheritedObjectType</b> member of an object-specific ACE.


### -field dwFlags

A set of inheritance flags that indicate the types of ACEs that can be inherited by the <b>pguid</b> object type. These flags correspond to the <b>AceFlags</b> member of an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure. This member can be a combination of the following values. 




					

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
The specified object type can inherit ACEs that have the CONTAINER_INHERIT_ACE flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The specified object type can inherit ACEs that have the INHERIT_ONLY_ACE flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The specified object type can inherit ACEs that have the OBJECT_INHERIT_ACE flag set.

</td>
</tr>
</table>
 


### -field pszName

A pointer to a null-terminated <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string containing a display string that describes the child object. 




Alternatively, <b>pszName</b> can be a string resource identifier returned by the 
<a href="_win32_makeintresource_cpp">MAKEINTRESOURCE</a> macro. Use the 
<a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">ISecurityInformation::GetObjectInformation</a> method to identify the module that contains the string resource.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>



<a href="https://msdn.microsoft.com/dafe6c45-616f-4339-a119-9b88055b5d3a">ISecurityInformation::GetInheritTypes</a>



<a href="https://msdn.microsoft.com/2bc63aa0-dada-4962-a381-6b0f8332e564">ISecurityInformation::GetObjectInformation</a>
 

 

