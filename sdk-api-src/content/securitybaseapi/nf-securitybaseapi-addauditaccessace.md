---
UID: NF:securitybaseapi.AddAuditAccessAce
title: AddAuditAccessAce function
author: windows-sdk-content
description: Adds a system-audit access control entry (ACE) to a system access control list (ACL). The access of a specified security identifier (SID) is audited.
old-location: security\addauditaccessace.htm
tech.root: SecAuthZ
ms.assetid: 34f22aea-9cde-411e-b2d5-bfcd3bfe325d
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AddAuditAccessAce, AddAuditAccessAce function [Security], _win32_addauditaccessace, security.addauditaccessace, securitybaseapi/AddAuditAccessAce
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
 - AddAuditAccessAce
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddAuditAccessAce function


## -description


The <b>AddAuditAccessAce</b> function adds a system-audit <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) to a system <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). The access of a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) is audited.

To control whether the new ACE can be inherited by child objects, use the 
<a href="https://msdn.microsoft.com/ddd1d815-c4ce-4572-982c-139e17cda192">AddAuditAccessAceEx</a> function.


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. This function adds a system-audit ACE to this ACL. The ACE is in the form of a 
<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a> structure.


### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.


### -param dwAccessMask [in]

Specifies the mask of access rights to be audited for the specified SID.


### -param pSid [in]

A pointer to the 
SID representing the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> whose access is being audited.


### -param bAuditSuccess [in]

Specifies whether successful access attempts are to be audited. Set this flag to <b>TRUE</b> to enable auditing; otherwise, set it to <b>FALSE</b>.


### -param bAuditFailure [in]

Specifies whether unsuccessful access attempts are to be audited. Set this flag to <b>TRUE</b> to enable auditing; otherwise, set it to <b>FALSE</b>.


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



The 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure placed in the ACE by the <b>AddAuditAccessAce</b> function specifies a type and size, but provides no ACE flags.




## -see-also




<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/ddd1d815-c4ce-4572-982c-139e17cda192">AddAuditAccessAceEx</a>



<a href="https://msdn.microsoft.com/02ce45ad-3d51-4548-848e-a62bf4bf72a8">DeleteAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/c26b5856-5447-4606-8110-f24a4d235c64">SYSTEM_AUDIT_ACE</a>
 

 

