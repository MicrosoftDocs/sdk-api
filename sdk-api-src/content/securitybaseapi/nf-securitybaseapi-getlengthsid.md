---
UID: NF:securitybaseapi.GetLengthSid
title: GetLengthSid function (securitybaseapi.h)
description: Returns the length, in bytes, of a valid security identifier (SID).
helpviewer_keywords: ["GetLengthSid","GetLengthSid function [Security]","_win32_getlengthsid","security.getlengthsid","securitybaseapi/GetLengthSid"]
old-location: security\getlengthsid.htm
tech.root: security
ms.assetid: 0acaa804-494c-4d69-b1f7-8d167b494761
ms.date: 12/05/2018
ms.keywords: GetLengthSid, GetLengthSid function [Security], _win32_getlengthsid, security.getlengthsid, securitybaseapi/GetLengthSid
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
 - GetLengthSid
 - securitybaseapi/GetLengthSid
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
 - GetLengthSid
---

# GetLengthSid function


## -description

The <b>GetLengthSid</b> function returns the length, in bytes, of a valid <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure whose length is returned. The structure is assumed to be valid.

## -returns

If the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is valid, the return value is the length, in bytes, of the <b>SID</b> structure.

If the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is not valid, the return value is undefined. Before calling <b>GetLengthSid</b>, pass the SID to the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a> function to verify that the SID is valid.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>