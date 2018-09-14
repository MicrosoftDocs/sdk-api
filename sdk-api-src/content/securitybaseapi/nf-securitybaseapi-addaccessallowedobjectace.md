---
UID: NF:securitybaseapi.AddAccessAllowedObjectAce
title: AddAccessAllowedObjectAce function
author: windows-sdk-content
description: Adds an access-allowed access control entry (ACE) to the end of a discretionary access control list (DACL).
old-location: security\addaccessallowedobjectace.htm
tech.root: secauthz
ms.assetid: ccf83e95-ba6f-49f5-a312-52eac90f209a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AddAccessAllowedObjectAce, AddAccessAllowedObjectAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, _win32_addaccessallowedobjectace, security.addaccessallowedobjectace, securitybaseapi/AddAccessAllowedObjectAce
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddAccessAllowedObjectAce
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddAccessAllowedObjectAce function


## -description


The <b>AddAccessAllowedObjectAce</b> function adds an access-allowed <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to the end of a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL). The new ACE can grant access to an object, or to a property set or property on an object. You can also use <b>AddAccessAllowedObjectAce</b> to add an ACE that only a specified type of child object can inherit.


## -parameters




### -param pAcl [in, out]

A pointer to a DACL. The <b>AddAccessAllowedObjectAce</b> function adds an access-allowed ACE to the end of this DACL. The ACE is in the form of an 
<a href="https://msdn.microsoft.com/ee91ca50-e81b-4872-95eb-349c2d5be004">ACCESS_ALLOWED_OBJECT_ACE</a> structure.


### -param dwAceRevision [in]

Specifies the revision level of the DACL being modified. This value must be ACL_REVISION_DS. If the DACL's revision level is lower than ACL_REVISION_DS, the function changes it to ACL_REVISION_DS.


### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure of the new ACE. This parameter can be a combination of the following values.

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
The ACE is inherited by container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs, while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by noncontainer objects.

</td>
</tr>
</table>
 


### -param AccessMask [in]

A set of bit flags that use the 
<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> format. These flags specify the access rights that the new ACE allows for the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


### -param ObjectTypeGuid [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies the type of object, property set, or property protected by the new ACE. If this parameter is <b>NULL</b>, the new ACE protects the object to which the DACL is assigned.


### -param InheritedObjectTypeGuid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies the type of object that can inherit the new ACE. If this parameter is non-<b>NULL</b>, only the specified object type can inherit the ACE. If <b>NULL</b>, any type of child object can inherit the ACE. In either case, inheritance is also controlled by the value of the <i>AceFlags</i> parameter, as well as by any protection against inheritance placed on the child objects.


### -param pSid [in]

A pointer to a 
SID that identifies the user, group, or <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> to which the new ACE allows access.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALLOTTED_SPACE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACL</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>AceFlags</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not structurally valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified revision is not known or is incompatible with that of the ACL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The ACE was successfully added.

</td>
</tr>
</table>
 




## -remarks



If both <i>ObjectTypeGuid</i> and <i>InheritedObjectTypeGuid</i> are <b>NULL</b>, use the 
<a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a> function rather than <b>AddAccessAllowedObjectAce</b>. This is suggested because an 
<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a> is smaller and more efficient than an 
<a href="https://msdn.microsoft.com/ee91ca50-e81b-4872-95eb-349c2d5be004">ACCESS_ALLOWED_OBJECT_ACE</a>.

The caller must ensure that ACEs are added to the DACL in the correct order. For more information, see 
<a href="https://msdn.microsoft.com/fccf043e-e769-4f3f-b18c-252be20190d8">Order of ACEs in a DACL</a>.




## -see-also




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/ee91ca50-e81b-4872-95eb-349c2d5be004">ACCESS_ALLOWED_OBJECT_ACE</a>



<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a>



<a href="https://msdn.microsoft.com/1427c908-92b6-46b2-9189-a2fd93c470b1">AddAccessDeniedObjectAce</a>



<a href="https://msdn.microsoft.com/be852a0c-9d96-4b29-b5f9-d9c41d838c12">AddAuditAccessObjectAce</a>



<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>
 

 

