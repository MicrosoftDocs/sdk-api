---
UID: NF:ntsecapi.LsaOpenPolicy
title: LsaOpenPolicy function (ntsecapi.h)
description: Opens a handle to the Policy object on a local or remote system.
helpviewer_keywords: ["LsaOpenPolicy","LsaOpenPolicy function [Security]","_lsa_lsaopenpolicy","ntsecapi/LsaOpenPolicy","security.lsaopenpolicy"]
old-location: security\lsaopenpolicy.htm
tech.root: security
ms.assetid: 361bc962-1e97-4606-a835-cbce37692c55
ms.date: 12/05/2018
ms.keywords: LsaOpenPolicy, LsaOpenPolicy function [Security], _lsa_lsaopenpolicy, ntsecapi/LsaOpenPolicy, security.lsaopenpolicy
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
 - LsaOpenPolicy
 - ntsecapi/LsaOpenPolicy
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
 - LsaOpenPolicy
---

# LsaOpenPolicy function


## -description

The <b>LsaOpenPolicy</b> function opens a handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object on a local or remote system.

You must run the process "As Administrator" so that the call doesn't fail with ERROR_ACCESS_DENIED.

## -parameters

### -param SystemName [in]

A pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the target system. The name can have the form "<i>ComputerName</i>" or "&#92;&#92;<i>ComputerName</i>". If this parameter is <b>NULL</b>, the function opens the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object on the local system.

### -param ObjectAttributes [in]

A pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_object_attributes">LSA_OBJECT_ATTRIBUTES</a> structure that specifies the connection attributes. The structure members are not used; initialize them to <b>NULL</b> or zero.

### -param DesiredAccess [in]

An <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> that specifies the requested access rights. The function fails if the DACL of the target system does not allow the caller the requested access. To determine the access rights that you need, see the documentation for the LSA functions with which you want to use the policy handle.

### -param PolicyHandle [in, out]

A pointer to an 
<a href="/windows/desktop/SecMgmt/lsa-handle">LSA_HANDLE</a> variable that receives a handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object.

When you no longer need this handle, pass it to the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaclose">LsaClose</a> function to close it.

## -returns

If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

To administer the local security policy of a local or remote system, you must call the <b>LsaOpenPolicy</b> function to establish a session with that system's LSA subsystem. <b>LsaOpenPolicy</b> connects to the LSA of the target system and returns a handle to the <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object of that system. You can use this handle in subsequent LSA function calls to administer the 
<a href="/windows/desktop/SecMgmt/local-security-policy">local security policy</a> information of the target system.

For an example that demonstrates calling this function see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

## -see-also

<a href="/windows/desktop/SecMgmt/lsa-handle">LSA_HANDLE</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_object_attributes">LSA_OBJECT_ATTRIBUTES</a>



<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaclose">LsaClose</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a>