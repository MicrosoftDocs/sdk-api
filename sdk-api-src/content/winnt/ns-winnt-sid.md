---
UID: NS:winnt._SID
title: SID (winnt.h)
description: Used to uniquely identify users or groups.
helpviewer_keywords: ["*PISID","PSID","PSID structure pointer [Security]","SID","SID structure [Security]","_SID","_win32_sid_str","security.sid","winnt/PSID","winnt/SID"]
old-location: security\sid.htm
tech.root: security
ms.assetid: 328fba4e-e590-4174-9274-52dad58cb91f
ms.date: 12/05/2018
ms.keywords: '*PISID, PSID, PSID structure pointer [Security], SID, SID structure [Security], _SID, _win32_sid_str, security.sid, winnt/PSID, winnt/SID'
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SID, *PISID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID
 - winnt/_SID
 - PISID
 - winnt/PISID
 - SID
 - winnt/SID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SID
---

# SID structure


## -description

The security identifier (SID) structure is a variable-length structure used to uniquely identify users or groups.
			

Applications should not modify a SID directly. To create and manipulate a security identifier, use the functions listed in the See Also section.

## -struct-fields

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida">ConvertSidToStringSid</a>



<a href="/windows/desktop/api/sddl/nf-sddl-convertstringsidtosida">ConvertStringSidToSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-copysid">CopySid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalsid">EqualSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-freesid">FreeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesid">InitializeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a>



<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>