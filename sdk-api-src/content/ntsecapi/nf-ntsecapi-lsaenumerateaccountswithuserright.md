---
UID: NF:ntsecapi.LsaEnumerateAccountsWithUserRight
title: LsaEnumerateAccountsWithUserRight function (ntsecapi.h)
description: Returns the accounts in the database of a Local Security Authority (LSA) Policy object that hold a specified privilege.
helpviewer_keywords: ["LsaEnumerateAccountsWithUserRight","LsaEnumerateAccountsWithUserRight function [Security]","_lsa_lsaenumerateaccountswithuserright","ntsecapi/LsaEnumerateAccountsWithUserRight","security.lsaenumerateaccountswithuserright"]
old-location: security\lsaenumerateaccountswithuserright.htm
tech.root: security
ms.assetid: 97e7180e-4edb-4edd-915e-0477e7e7a9ff
ms.date: 12/05/2018
ms.keywords: LsaEnumerateAccountsWithUserRight, LsaEnumerateAccountsWithUserRight function [Security], _lsa_lsaenumerateaccountswithuserright, ntsecapi/LsaEnumerateAccountsWithUserRight, security.lsaenumerateaccountswithuserright
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaEnumerateAccountsWithUserRight
 - ntsecapi/LsaEnumerateAccountsWithUserRight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsapolicy-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaEnumerateAccountsWithUserRight
---

# LsaEnumerateAccountsWithUserRight function


## -description

The <b>LsaEnumerateAccountsWithUserRight</b> function returns the accounts in the database of a <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object that hold a specified <a href="/windows/desktop/SecGloss/p-gly">privilege</a>. The accounts returned by this function hold the specified privilege directly through the user account, not as part of membership to a group.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have POLICY_LOOKUP_NAMES and POLICY_VIEW_LOCAL_INFORMATION user rights. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param UserRight [in]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that specifies the name of a privilege. For a list of privileges, see 
<a href="/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a> and 
Account Rights Constants. 




If this parameter is <b>NULL</b>, the function enumerates all accounts in the LSA database of the system associated with the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object.

### -param Buffer [out]

Pointer to a variable that receives a pointer to an array of 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_enumeration_information">LSA_ENUMERATION_INFORMATION</a> structures. The <b>Sid</b> member of each structure is a pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of an account that holds the specified privilege. 




When you no longer need the information, free the memory by passing the returned pointer to 
the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function.

### -param CountReturned [out]

Pointer to a variable that receives the number of entries returned in the <i>EnumerationBuffer</i> parameter.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be one of the following values or one of the 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

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
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_enumeration_information">LSA_ENUMERATION_INFORMATION</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a>