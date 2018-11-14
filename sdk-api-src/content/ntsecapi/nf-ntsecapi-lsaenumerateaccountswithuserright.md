---
UID: NF:ntsecapi.LsaEnumerateAccountsWithUserRight
title: LsaEnumerateAccountsWithUserRight function
author: windows-sdk-content
description: Returns the accounts in the database of a Local Security Authority (LSA) Policy object that hold a specified privilege.
old-location: security\lsaenumerateaccountswithuserright.htm
tech.root: secmgmt
ms.assetid: 97e7180e-4edb-4edd-915e-0477e7e7a9ff
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LsaEnumerateAccountsWithUserRight, LsaEnumerateAccountsWithUserRight function [Security], _lsa_lsaenumerateaccountswithuserright, ntsecapi/LsaEnumerateAccountsWithUserRight, security.lsaenumerateaccountswithuserright
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaEnumerateAccountsWithUserRight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LsaEnumerateAccountsWithUserRight
: 
---

# LsaEnumerateAccountsWithUserRight function


## -description


The <b>LsaEnumerateAccountsWithUserRight</b> function returns the accounts in the database of a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object that hold a specified <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privilege</a>. The accounts returned by this function hold the specified privilege directly through the user account, not as part of membership to a group.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have POLICY_LOOKUP_NAMES and POLICY_VIEW_LOCAL_INFORMATION user rights. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param UserRight [in]

Pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the name of a privilege. For a list of privileges, see 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Privilege Constants</a> and 
Account Rights Constants. 




If this parameter is <b>NULL</b>, the function enumerates all accounts in the LSA database of the system associated with the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object.


### -param Buffer [out]

Pointer to a variable that receives a pointer to an array of 
<a href="https://msdn.microsoft.com/7577548f-3ceb-43a5-b447-6f66a09963fe">LSA_ENUMERATION_INFORMATION</a> structures. The <b>Sid</b> member of each structure is a pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of an account that holds the specified privilege. 




When you no longer need the information, free the memory by passing the returned pointer to 
the <a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a> function.


### -param CountReturned [out]

Pointer to a variable that receives the number of entries returned in the <i>EnumerationBuffer</i> parameter.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be one of the following values or one of the 
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
The privilege string specified was not a valid privilege.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
There were no accounts with the specified privilege.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/7577548f-3ceb-43a5-b447-6f66a09963fe">LSA_ENUMERATION_INFORMATION</a>



<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>



<a href="https://msdn.microsoft.com/361bc962-1e97-4606-a835-cbce37692c55">LsaOpenPolicy</a>
 

 

