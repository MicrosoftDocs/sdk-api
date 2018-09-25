---
UID: NF:ntsecapi.LsaEnumerateAccountRights
title: LsaEnumerateAccountRights function
author: windows-sdk-content
description: The LsaEnumerateAccountRights function enumerates the privileges assigned to an account.
old-location: security\lsaenumerateaccountrights.htm
tech.root: SecMgmt
ms.assetid: 3f4a4a9a-66ca-410a-8bdc-c390e8b966e3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LsaEnumerateAccountRights, LsaEnumerateAccountRights function [Security], _lsa_lsaenumerateaccountrights, ntsecapi/LsaEnumerateAccountRights, security.lsaenumerateaccountrights
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
 - LsaEnumerateAccountRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaEnumerateAccountRights function


## -description


The <b>LsaEnumerateAccountRights</b> function enumerates the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a> assigned to an account.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the SID of the account for which to enumerate privileges.


### -param UserRights [out]

Receives a pointer to an array of 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege held by the account. For a list of privilege names, see 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Privilege Constants</a>

When you no longer need the information, pass the returned pointer to 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>.


### -param CountOfRights [out]

Pointer to a variable that receives the number of privileges in the <i>UserRights</i> array.


## -returns



If at least one account right is found, the function succeeds and returns STATUS_SUCCESS.

If no account rights are found or if the function fails for any other reason, the function returns an NTSTATUS code such as FILE_NOT_FOUND. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>. Use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/66b78404-02c2-48e9-92c3-d27b68f77c23">LsaAddAccountRights</a>



<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>



<a href="https://msdn.microsoft.com/ad250a01-7a24-4fae-975c-aa3e65731c82">LsaRemoveAccountRights</a>
 

 

