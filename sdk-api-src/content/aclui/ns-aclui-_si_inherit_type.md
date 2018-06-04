---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

