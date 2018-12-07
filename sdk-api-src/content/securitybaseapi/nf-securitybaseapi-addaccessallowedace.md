---
UID: NF:securitybaseapi.AddAccessAllowedAce
title: AddAccessAllowedAce function
author: windows-sdk-content
description: Adds an access-allowed access control entry (ACE) to an access control list (ACL). The access is granted to a specified security identifier (SID).
old-location: security\addaccessallowedace.htm
tech.root: secauthz
ms.assetid: 1004353a-f907-4452-9c0f-85eba0ece813
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddAccessAllowedAce, AddAccessAllowedAce function [Security], _win32_addaccessallowedace, security.addaccessallowedace, securitybaseapi/AddAccessAllowedAce
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - AddAccessAllowedAce
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddAccessAllowedAce function


## -description


The <b>AddAccessAllowedAce</b> function adds an access-allowed <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). The access is granted to a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).

To control whether the new ACE can be inherited by child objects, use the 
<a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a> function.


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. This function adds an access-allowed ACE to the end of this ACL. The ACE is in the form of an 
<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a> structure.


### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.


### -param AccessMask [in]

Specifies the mask of access rights to be granted to the specified SID.


### -param pSid [in]

A pointer to the 
SID  representing a user, group, or logon account being granted access.


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



The addition of an access-allowed ACE to an ACL is the most common form of ACL modification.

The <b>AddAccessAllowedAce</b> and <a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a> functions add a new ACE to the end of the list of ACEs for the ACL. These functions do not automatically place the new ACE in the proper canonical order. It is the caller's responsibility to ensure that the ACL is in canonical order by adding ACEs in the proper sequence.

The 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure placed in the ACE by the <b>AddAccessAllowedAce</b> function specifies a type and size, but provides no inheritance and no ACE flags.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/9e9ed9b7-ea23-4dec-8b92-a86aa81267ab">Starting an Interactive Client Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/6ddec01f-237f-4b6a-8ea8-a126017b30c5">AddAccessAllowedAceEx</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/34f22aea-9cde-411e-b2d5-bfcd3bfe325d">AddAuditAccessAce</a>



<a href="https://msdn.microsoft.com/02ce45ad-3d51-4548-848e-a62bf4bf72a8">DeleteAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>
 

 

