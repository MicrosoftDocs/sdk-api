---
UID: NF:ntsecapi.LsaRemoveAccountRights
title: LsaRemoveAccountRights function (ntsecapi.h)
description: Removes one or more privileges from an account.
helpviewer_keywords: ["LsaRemoveAccountRights","LsaRemoveAccountRights function [Security]","_lsa_lsaremoveaccountrights","ntsecapi/LsaRemoveAccountRights","security.lsaremoveaccountrights"]
old-location: security\lsaremoveaccountrights.htm
tech.root: security
ms.assetid: ad250a01-7a24-4fae-975c-aa3e65731c82
ms.date: 12/05/2018
ms.keywords: LsaRemoveAccountRights, LsaRemoveAccountRights function [Security], _lsa_lsaremoveaccountrights, ntsecapi/LsaRemoveAccountRights, security.lsaremoveaccountrights
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
 - LsaRemoveAccountRights
 - ntsecapi/LsaRemoveAccountRights
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
 - LsaRemoveAccountRights
---

# LsaRemoveAccountRights function


## -description

The <b>LsaRemoveAccountRights</b> function removes one or more <a href="/windows/desktop/SecGloss/p-gly">privileges</a> from an account. You can specify the privileges to be removed, or you can set a flag to remove all privileges. When you remove all privileges, the function deletes the account. If you specify privileges not held by the account, the function ignores them.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param AccountSid [in]

Pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the account from which the privileges are removed.

### -param AllRights [in]

If <b>TRUE</b>, the function removes all privileges and deletes the account. In this case, the function ignores the <i>UserRights</i> parameter. If <b>FALSE</b>, the function removes the privileges specified by the <i>UserRights</i> parameter.

### -param UserRights [in]

Pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege to be removed from the account. For a list of privilege names, see 
<a href="/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a>.

### -param CountOfRights [in]

Specifies the number of elements in the <i>UserRights</i> array.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
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
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights">LsaAddAccountRights</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights">LsaEnumerateAccountRights</a>