---
UID: NF:aclapi.TreeResetNamedSecurityInfoW
title: TreeResetNamedSecurityInfoW function
author: windows-sdk-content
description: Resets specified security information in the security descriptor of a specified tree of objects.
old-location: security\treeresetnamedsecurityinfo.htm
tech.root: SecAuthZ
ms.assetid: adae7d07-a452-409e-b1a1-e9f86f873e39
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: TreeResetNamedSecurityInfo, TreeResetNamedSecurityInfo function [Security], TreeResetNamedSecurityInfoA, TreeResetNamedSecurityInfoW, aclapi/TreeResetNamedSecurityInfo, aclapi/TreeResetNamedSecurityInfoA, aclapi/TreeResetNamedSecurityInfoW, security.treeresetnamedsecurityinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TreeResetNamedSecurityInfoW (Unicode) and TreeResetNamedSecurityInfoA (ANSI)
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
 - Ext-MS-Win-AdvAPI32-ntmarta-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - TreeResetNamedSecurityInfo
 - TreeResetNamedSecurityInfoA
 - TreeResetNamedSecurityInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TreeResetNamedSecurityInfoW function


## -description


The <b>TreeResetNamedSecurityInfo</b> function resets specified security information in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of a specified tree of objects. This function allows a specified  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) or any elements in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) to be propagated throughout an entire tree. This function supports a callback function to track the progress of the tree operation.


## -parameters




### -param pObjectName [in]

			Pointer to a <b>null</b>-terminated string that specifies the name of the root node object for the objects  that are to receive updated security information. Supported objects are registry keys and file objects. For descriptions of the string formats for the different object types, see 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>.


### -param ObjectType [in]

A value of the <a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>  enumeration  that indicates the type of object named by the <i>pObjectName</i> parameter. The supported values are SE_REGISTRY_KEY and SE_FILE_OBJECT, for registry keys and file objects, respectively. 


### -param SecurityInfo [in]

A set of 
bit flags that indicate the type of security information to reset. This parameter can be a combination of the 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> bit flags.


### -param pOwner [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the owner of the object. The SID must be one that can be assigned as the owner SID of a security descriptor. The <i>SecurityInfo</i> parameter must include the OWNER_SECURITY_INFORMATION flag. To set the owner, the caller must have WRITE_OWNER access to each object, including the root object. If you are not setting the owner SID, this parameter can be <b>NULL</b>.


### -param pGroup [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the primary group of the object. The <i>SecurityInfo</i> parameter must include the GROUP_SECURITY_INFORMATION flag.  To set the group, the caller must have WRITE_OWNER access to each object, including the root object. If you are not setting the primary group SID, this parameter can be <b>NULL</b>.


### -param pDacl [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) structure that represents the new DACL for the objects being reset. The <i>SecurityInfo</i> parameter must include the DACL_SECURITY_INFORMATION flag. The caller must have READ_CONTROL and WRITE_DAC access to each  object, including the root object. If you are not setting the DACL, this parameter can be <b>NULL</b>.


### -param pSacl [in, optional]

A pointer to an ACL structure that represents the new SACL for the objects being reset.  The <i>SecurityInfo</i> parameter must include any of the following flags: SACL_SECURITY_INFORMATION, LABEL_SECURITY_INFORMATION, ATTRIBUTE_SECURITY_INFORMATION, SCOPE_SECURITY_INFORMATION, or BACKUP_SECURITY_INFORMATION. If setting SACL_SECURITY_INFORMATION or SCOPE_SECURITY_INFORMATION, the caller must have the SE_SECURITY_NAME privilege enabled. If you are not setting the SACL, this parameter can be <b>NULL</b>.


### -param KeepExplicit [in]

Boolean value that defines whether explicitly defined ACEs are kept or deleted for the sub-tree. If  <i>KeepExplicit</i> is <b>TRUE</b>, then explicitly defined ACEs are kept for each subtree DACL and SACL, and inherited ACEs are replaced by the inherited ACEs from <i>pDacl</i> and <i>pSacl</i>.  If  <i>KeepExplicit</i> is <b>FALSE</b>, then explicitly defined ACEs for each subtree DACL and SACL are deleted before the inherited ACEs are replaced by the inherited ACEs from <i>pDacl</i> and <i>pSacl</i>.


### -param fnProgress [in, optional]

A pointer to the function used to track the progress of the <b>TreeResetNamedSecurityInfo</b> function. The prototype of the progress function is:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Aclapi.h&gt;

typedef VOID (*FN_PROGRESS) (
  IN LPWSTR pObjectName,              // Name of object just processed
  IN DWORD Status,                    // Status of operation on object
  IN OUT PPROG_INVOKE_SETTING pInvokeSetting, // When to set
  IN PVOID Args,                      // Caller specific data
  IN BOOL SecuritySet                 // Whether security was set
);
</pre>
</td>
</tr>
</table></span></div>
The progress function provides the caller with progress and error information when nodes are processed. The caller specifies the progress function in <i>fnProgress</i>, and during the tree  operation, <b>TreeResetNamedSecurityInfo</b> passes the name of the last object processed, the error status of that operation, and the current  PROG_INVOKE_SETTING value. The caller can change the PROG_INVOKE_SETTING value by using <i>pInvokeSetting</i>.

If no progress function is to be used, set this parameter to <b>NULL</b>.


### -param ProgressInvokeSetting [in]

A value of the <a href="https://msdn.microsoft.com/3eee30d6-7d9d-468f-b6ba-e172da523169">PROG_INVOKE_SETTING</a> enumeration that specifies the initial setting for the progress function.


### -param Args [in, optional]

A pointer to a <b>VOID</b> for progress function arguments specified by the caller.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns an error code defined in WinError.h.




## -remarks



Setting a <b>NULL</b> owner, group, DACL, or SACL is not supported by this function.

If the caller does not contain the proper privileges and permissions to support the requested owner, group, DACL, and SACL updates, then none of the updates are performed.

This function is similar to the <a href="https://msdn.microsoft.com/caa711c3-301b-4ed7-b1f4-dc6a48563905">TreeSetNamedSecurityInfo</a> function:

<ul>
<li>If the <i>KeepExplicit</i> parameter of <b>TreeResetNamedSecurityInfo</b> is set to <b>TRUE</b>, then the function is equivalent to  <a href="https://msdn.microsoft.com/caa711c3-301b-4ed7-b1f4-dc6a48563905">TreeSetNamedSecurityInfo</a> with the  <i>dwAction</i> parameter set to  TREE_SEC_INFO_RESET_KEEP_EXPLICIT.</li>
<li>If the <i>KeepExplicit</i> parameter of <b>TreeResetNamedSecurityInfo</b> is set to <b>FALSE</b>, then the function is equivalent to  <a href="https://msdn.microsoft.com/caa711c3-301b-4ed7-b1f4-dc6a48563905">TreeSetNamedSecurityInfo</a> with the  <i>dwAction</i>parameter set to  TREE_SEC_INFO_RESET.</li>
</ul>


