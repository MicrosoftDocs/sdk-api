---
UID: NF:ntsecapi.LsaRemoveAccountRights
title: LsaRemoveAccountRights function
author: windows-sdk-content
description: Removes one or more privileges from an account.
old-location: security\lsaremoveaccountrights.htm
old-project: secmgmt
ms.assetid: ad250a01-7a24-4fae-975c-aa3e65731c82
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LsaRemoveAccountRights, LsaRemoveAccountRights function [Security], _lsa_lsaremoveaccountrights, ntsecapi/LsaRemoveAccountRights, security.lsaremoveaccountrights
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaRemoveAccountRights
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaRemoveAccountRights function


## -description


The <b>LsaRemoveAccountRights</b> function removes one or more <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a> from an account. You can specify the privileges to be removed, or you can set a flag to remove all privileges. When you remove all privileges, the function deletes the account. If you specify privileges not held by the account, the function ignores them.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the account from which the privileges are removed.


### -param AllRights [in]

If <b>TRUE</b>, the function removes all privileges and deletes the account. In this case, the function ignores the <i>UserRights</i> parameter. If <b>FALSE</b>, the function removes the privileges specified by the <i>UserRights</i> parameter.


### -param UserRights [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege to be removed from the account. For a list of privilege names, see 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Privilege Constants</a>.


### -param CountOfRights [in]

Specifies the number of elements in the <i>UserRights</i> array.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PRIVILEGE</b></dt>
</dl>
</td>
<td width="60%">
One of the privilege names is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Indicates the <i>UserRights</i> parameter was <b>NULL</b> and the <i>AllRights</i> parameter was <b>FALSE</b>.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/66b78404-02c2-48e9-92c3-d27b68f77c23">LsaAddAccountRights</a>



<a href="https://msdn.microsoft.com/3f4a4a9a-66ca-410a-8bdc-c390e8b966e3">LsaEnumerateAccountRights</a>
 

 

