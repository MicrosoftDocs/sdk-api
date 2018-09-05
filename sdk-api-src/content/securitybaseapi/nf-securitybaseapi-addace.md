---
UID: NF:securitybaseapi.AddAce
title: AddAce function
author: windows-sdk-content
description: Adds one or more access control entries (ACEs) to a specified access control list (ACL).
old-location: security\addace.htm
old-project: SecAuthZ
ms.assetid: f472d864-a273-49b5-b5e2-98772989971e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddAce, AddAce function [Security], _win32_addace, security.addace, securitybaseapi/AddAce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
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
 - AddAce
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# AddAce function


## -description


The <b>AddAce</b> function adds one or more <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) to a specified <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. This function adds an ACE to this ACL.


### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs. This value must be compatible with the <b>AceType</b> field of all ACEs in <i>pAceList</i>. 
 Otherwise, the function will fail and set the last error to ERROR_INVALID_PARAMETER.


### -param dwStartingAceIndex [in]

Specifies the position in the ACL's list of ACEs at which to add new ACEs. A value of zero inserts the ACEs at the beginning of the list. A value of MAXDWORD appends the ACEs to the end of the list.


### -param pAceList [in]

A pointer to a list of one or more ACEs to be added to the specified ACL. The ACEs in the list must be stored contiguously.


### -param nAceListLength [in]

Specifies the size, in bytes, of the input buffer pointed to by the <i>pAceList</i> parameter.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

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



Applications frequently use the 
<a href="https://msdn.microsoft.com/bf770761-008a-4a35-b31f-b781d5a8622b">FindFirstFreeAce</a> and 
<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a> functions when using the <b>AddAce</b> function to manipulate an ACL. In addition, the 
<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a> structure retrieved by the 
<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a> function contains the size of the ACL and the number of ACEs it contains.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/9e9ed9b7-ea23-4dec-8b92-a86aa81267ab">Starting an Interactive Client Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a>



<a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/34f22aea-9cde-411e-b2d5-bfcd3bfe325d">AddAuditAccessAce</a>



<a href="https://msdn.microsoft.com/02ce45ad-3d51-4548-848e-a62bf4bf72a8">DeleteAce</a>



<a href="https://msdn.microsoft.com/bf770761-008a-4a35-b31f-b781d5a8622b">FindFirstFreeAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>
 

 

