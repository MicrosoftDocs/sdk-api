---
UID: NF:securitybaseapi.IsWellKnownSid
title: IsWellKnownSid function (securitybaseapi.h)
description: Compares a SID to a well-known SID and returns TRUE if they match.
helpviewer_keywords: ["IsWellKnownSid","IsWellKnownSid function [Security]","_win32_iswellknownsid","security.iswellknownsid","securitybaseapi/IsWellKnownSid"]
old-location: security\iswellknownsid.htm
tech.root: security
ms.assetid: 1a08c70c-00fa-4c62-883d-4f17f9d7c04b
ms.date: 12/05/2018
ms.keywords: IsWellKnownSid, IsWellKnownSid function [Security], _win32_iswellknownsid, security.iswellknownsid, securitybaseapi/IsWellKnownSid
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
 - IsWellKnownSid
 - securitybaseapi/IsWellKnownSid
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
 - IsWellKnownSid
---

# IsWellKnownSid function


## -description

The <b>IsWellKnownSid</b> function compares a SID to a well-known SID and returns <b>TRUE</b> if they match.

## -parameters

### -param pSid [in]

A pointer to the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> to test.

### -param WellKnownSidType [in]

Member of the 
<a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WELL_KNOWN_SID_TYPE</a> enumeration to compare with the SID at <i>pSid</i>.

## -returns

Returns <b>TRUE</b> if the SID at <i>pSid</i> matches the well-known SID indicated by <i>WellKnownSidType</i>.

Otherwise, returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ne-winnt-well_known_sid_type">WELL_KNOWN_SID_TYPE</a>