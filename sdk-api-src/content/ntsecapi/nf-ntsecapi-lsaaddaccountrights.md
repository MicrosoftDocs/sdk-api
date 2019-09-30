---
UID: NF:ntsecapi.LsaAddAccountRights
title: LsaAddAccountRights function (ntsecapi.h)
author: windows-sdk-content
description: Assigns one or more privileges to an account.
old-location: security\lsaaddaccountrights.htm
tech.root: SecMgmt
ms.assetid: 66b78404-02c2-48e9-92c3-d27b68f77c23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LsaAddAccountRights, LsaAddAccountRights function [Security], _lsa_lsaaddaccountrights, ntsecapi/LsaAddAccountRights, security.lsaaddaccountrights
ms.topic: function
f1_keywords:
- ntsecapi/LsaAddAccountRights
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
- LsaAddAccountRights
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LsaAddAccountRights function


## -description


The <b>LsaAddAccountRights</b> function assigns one or more <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">privileges</a> to an account. If the account does not exist, <b>LsaAddAccountRights</b> creates it.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://docs.microsoft.com/windows/desktop/SecMgmt/policy-object">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. If the account identified by the <i>AccountSid</i> parameter does not exist, the handle must have the POLICY_CREATE_ACCOUNT access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the SID of the account to which the function assigns <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">privileges</a>.


### -param UserRights [in]

Pointer to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege to add to the account. For a list of privilege names, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-constants">Privilege Constants</a>.


### -param CountOfRights [in]

Specifies the number of elements in the <i>UserRights</i> array.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

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
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



If you specify privileges already granted to the account, they are ignored.

For an example that demonstrates calling this function, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/managing-account-permissions">Managing Account Permissions</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights">LsaEnumerateAccountRights</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights">LsaRemoveAccountRights</a>
 

 

