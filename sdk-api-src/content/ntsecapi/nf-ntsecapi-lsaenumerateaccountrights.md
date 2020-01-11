---
UID: NF:ntsecapi.LsaEnumerateAccountRights
title: LsaEnumerateAccountRights function (ntsecapi.h)
description: The LsaEnumerateAccountRights function enumerates the privileges assigned to an account.
old-location: security\lsaenumerateaccountrights.htm
tech.root: SecMgmt
ms.assetid: 3f4a4a9a-66ca-410a-8bdc-c390e8b966e3
ms.date: 12/05/2018
ms.keywords: LsaEnumerateAccountRights, LsaEnumerateAccountRights function [Security], _lsa_lsaenumerateaccountrights, ntsecapi/LsaEnumerateAccountRights, security.lsaenumerateaccountrights
f1_keywords:
- ntsecapi/LsaEnumerateAccountRights
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LsaEnumerateAccountRights function


## -description


The <b>LsaEnumerateAccountRights</b> function enumerates the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">privileges</a> assigned to an account.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://docs.microsoft.com/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the SID of the account for which to enumerate privileges.


### -param UserRights [out]

Receives a pointer to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege held by the account. For a list of privilege names, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a>

When you no longer need the information, pass the returned pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>.


### -param CountOfRights [out]

Pointer to a variable that receives the number of privileges in the <i>UserRights</i> array.


## -returns



If at least one account right is found, the function succeeds and returns STATUS_SUCCESS.

If no account rights are found or if the function fails for any other reason, the function returns an NTSTATUS code such as FILE_NOT_FOUND. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>. Use the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights">LsaAddAccountRights</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights">LsaRemoveAccountRights</a>
 

 

