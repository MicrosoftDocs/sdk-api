---
UID: NF:securitybaseapi.InitializeSid
title: InitializeSid function (securitybaseapi.h)
author: windows-sdk-content
description: Initializes a security identifier (SID).
old-location: security\initializesid.htm
tech.root: SecAuthZ
ms.assetid: b2d803a5-faaf-4066-ba2c-0442c71bb150
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeSid, InitializeSid function [Security], _win32_initializesid, security.initializesid, securitybaseapi/InitializeSid
ms.topic: function
f1_keywords: 
 - "securitybaseapi/InitializeSid"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - InitializeSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InitializeSid function


## -description


The <b>InitializeSid</b> function initializes a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).


## -parameters




### -param Sid [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a> structure to be initialized.


### -param pIdentifierAuthority [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure to set in the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a> structure.


### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to set in the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a>. Values of the subauthority must be set separately, as described in the following Remarks section.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Although the <b>InitializeSid</b> function sets the number of subauthorities for the SID, it does not set the subauthority values. This must be done separately, using functions such as <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>.

An application can use the <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a> function to initialize a SID and set its subauthority values.

This function uses a 32-bit RID value. For applications that require a larger RID value, use 
<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a>
 

 

