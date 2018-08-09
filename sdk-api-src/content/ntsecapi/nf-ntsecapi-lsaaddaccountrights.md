---
UID: NF:ntsecapi.LsaAddAccountRights
title: LsaAddAccountRights function
author: windows-sdk-content
description: Assigns one or more privileges to an account.
old-location: security\lsaaddaccountrights.htm
old-project: secmgmt
ms.assetid: 66b78404-02c2-48e9-92c3-d27b68f77c23
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LsaAddAccountRights, LsaAddAccountRights function [Security], _lsa_lsaaddaccountrights, ntsecapi/LsaAddAccountRights, security.lsaaddaccountrights
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
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
 - LsaAddAccountRights
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaAddAccountRights function


## -description


The <b>LsaAddAccountRights</b> function assigns one or more <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> to an account. If the account does not exist, <b>LsaAddAccountRights</b> creates it.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. If the account identified by the <i>AccountSid</i> parameter does not exist, the handle must have the POLICY_CREATE_ACCOUNT access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the SID of the account to which the function assigns <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a>.


### -param UserRights [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege to add to the account. For a list of privilege names, see 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Privilege Constants</a>.


### -param CountOfRights [in]

Specifies the number of elements in the <i>UserRights</i> array.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
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
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



If you specify privileges already granted to the account, they are ignored.

For an example that demonstrates calling this function, see 
<a href="https://msdn.microsoft.com/c28c03f0-4638-42ed-8dad-1e934cf99273">Managing Account Permissions</a>.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/3f4a4a9a-66ca-410a-8bdc-c390e8b966e3">LsaEnumerateAccountRights</a>



<a href="https://msdn.microsoft.com/ad250a01-7a24-4fae-975c-aa3e65731c82">LsaRemoveAccountRights</a>
 

 

