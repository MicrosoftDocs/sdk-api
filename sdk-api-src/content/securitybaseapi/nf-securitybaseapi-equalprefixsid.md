---
UID: NF:securitybaseapi.EqualPrefixSid
title: EqualPrefixSid function (securitybaseapi.h)
description: Tests two security-identifier (SID) prefix values for equality. A SID prefix is the entire SID except for the last subauthority value.
helpviewer_keywords: ["EqualPrefixSid","EqualPrefixSid function [Security]","_win32_equalprefixsid","security.equalprefixsid","securitybaseapi/EqualPrefixSid"]
old-location: security\equalprefixsid.htm
tech.root: security
ms.assetid: ef41de63-4ab5-40c6-8b16-b960e1308b5b
ms.date: 12/05/2018
ms.keywords: EqualPrefixSid, EqualPrefixSid function [Security], _win32_equalprefixsid, security.equalprefixsid, securitybaseapi/EqualPrefixSid
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - EqualPrefixSid
 - securitybaseapi/EqualPrefixSid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - EqualPrefixSid
---

# EqualPrefixSid function


## -description

The <b>EqualPrefixSid</b> function tests two <a href="/windows/desktop/SecGloss/s-gly">security-identifier</a> (SID) prefix values for equality. A SID prefix is the entire SID except for the last subauthority value.

## -parameters

### -param pSid1 [in]

A pointer to the first 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to compare. This structure is assumed to be valid.

### -param pSid2 [in]

A pointer to the second <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to compare. This structure is assumed to be valid.

## -returns

If the SID prefixes are equal, the return value is nonzero.

If the SID prefixes are not equal, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>EqualPrefixSid</b> function enables a server application in one domain to verify an attempt by a user to log on to another domain. For example, if a user attempts to log on to RemoteDomain from a workstation in LocalDomain, the server for LocalDomain can request the SIDs for the user and the user's groups from RemoteDomain. The domain controller for RemoteDomain responds with the relevant SIDs.

All SIDs for a specified domain have the same prefix. When the server receives the user's SIDs, the server can call the <b>EqualPrefixSid</b> function for each SID, comparing the user or group SID against the SID for RemoteDomain. If any of the SID prefixes are not equal, the server refuses the logon attempt.

It is advisable to modify the SID for a domain before comparing it with a group or user SID. If the SID for RemoteDomain is S-1–1234–8, each group or user SID for that domain has S-1–1234–8 as its prefix. To compare the SIDs by using the <b>EqualPrefixSid</b> function, an application copies the domain SID and adds any subauthority (<a href="/windows/desktop/SecGloss/r-gly">RID</a>) value to the copy, thereby creating a SID in the form S-1–1234–8–0. The application then uses the modified domain SID as a template against which the group and user SIDs are compared.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-copysid">CopySid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalsid">EqualSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>