---
UID: NF:securitybaseapi.CreateWellKnownSid
title: CreateWellKnownSid function (securitybaseapi.h)
description: Creates a SID for predefined aliases.
helpviewer_keywords: ["CreateWellKnownSid","CreateWellKnownSid function [Security]","_win32_createwellknownsid","security.createwellknownsid","securitybaseapi/CreateWellKnownSid"]
old-location: security\createwellknownsid.htm
tech.root: security
ms.assetid: 00e75bae-fbce-41a3-a0bc-c345c36f2c84
ms.date: 12/05/2018
ms.keywords: CreateWellKnownSid, CreateWellKnownSid function [Security], _win32_createwellknownsid, security.createwellknownsid, securitybaseapi/CreateWellKnownSid
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
 - CreateWellKnownSid
 - securitybaseapi/CreateWellKnownSid
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
 - CreateWellKnownSid
---

# CreateWellKnownSid function


## -description

The <b>CreateWellKnownSid</b> function creates a SID for predefined aliases.

## -parameters

### -param WellKnownSidType [in]

Member of the <a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WELL_KNOWN_SID_TYPE</a> enumeration that specifies what the SID will identify.

### -param DomainSid [in, optional]

A pointer to a SID that identifies the domain to use when creating the SID. Pass <b>NULL</b> to use the local computer.

### -param pSid [out, optional]

A pointer to memory where <b>CreateWellKnownSid</b> will store the new SID.

### -param cbSid [in, out]

A pointer to a <b>DWORD</b> that contains the number of bytes available at <i>pSid</i>. The <b>CreateWellKnownSid</b> function stores the number of bytes actually used at this location.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equaldomainsid">EqualDomainSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getwindowsaccountdomainsid">GetWindowsAccountDomainSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-iswellknownsid">IsWellKnownSid</a>



<a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WELL_KNOWN_SID_TYPE</a>