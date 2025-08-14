---
UID: NF:securitybaseapi.GetWindowsAccountDomainSid
title: GetWindowsAccountDomainSid function (securitybaseapi.h)
description: Receives a security identifier (SID) and returns a SID representing the domain of that SID.
helpviewer_keywords: ["GetWindowsAccountDomainSid","GetWindowsAccountDomainSid function [Security]","_win32_getwindowsaccountdomainsid","security.getwindowsaccountdomainsid","securitybaseapi/GetWindowsAccountDomainSid"]
old-location: security\getwindowsaccountdomainsid.htm
tech.root: security
ms.assetid: ee2ba1b4-1bef-4d79-bb18-512705e2c378
ms.date: 12/05/2018
ms.keywords: GetWindowsAccountDomainSid, GetWindowsAccountDomainSid function [Security], _win32_getwindowsaccountdomainsid, security.getwindowsaccountdomainsid, securitybaseapi/GetWindowsAccountDomainSid
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetWindowsAccountDomainSid
 - securitybaseapi/GetWindowsAccountDomainSid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetWindowsAccountDomainSid
---

# GetWindowsAccountDomainSid function


## -description

The <b>GetWindowsAccountDomainSid</b> function receives a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) and returns a SID representing the domain of that SID.

## -parameters

### -param pSid [in]

A pointer to the SID to examine.

### -param pDomainSid [out, optional]

Pointer that <b>GetWindowsAccountDomainSid</b> fills with a pointer to a SID representing the domain.

### -param cbDomainSid [in, out]

A pointer to a <b>DWORD</b> that <b>GetWindowsAccountDomainSid</b> fills with the size of the domain SID, in bytes.

## -returns

Returns <b>TRUE</b> if successful.

Otherwise, returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.