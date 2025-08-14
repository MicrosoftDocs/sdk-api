---
UID: NF:ntsecapi.LsaDeleteTrustedDomain
title: LsaDeleteTrustedDomain function (ntsecapi.h)
description: The LsaDeleteTrustedDomain function removes a trusted domain from the list of trusted domains for a system and deletes the associated TrustedDomain object.
helpviewer_keywords: ["LsaDeleteTrustedDomain","LsaDeleteTrustedDomain function [Security]","_lsa_lsadeletetrusteddomain","ntsecapi/LsaDeleteTrustedDomain","security.lsadeletetrusteddomain"]
old-location: security\lsadeletetrusteddomain.htm
tech.root: security
ms.assetid: 4a7afa28-1786-4a58-a955-d2d8b12e62e4
ms.date: 12/05/2018
ms.keywords: LsaDeleteTrustedDomain, LsaDeleteTrustedDomain function [Security], _lsa_lsadeletetrusteddomain, ntsecapi/LsaDeleteTrustedDomain, security.lsadeletetrusteddomain
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
 - LsaDeleteTrustedDomain
 - ntsecapi/LsaDeleteTrustedDomain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-lsa-l1-1-4.dll
 - ext-ms-win-advapi32-lsa-l1-1-3.dll
 - ext-ms-win-advapi32-lsa-l1-1-2.dll
 - Advapi32.dll
api_name:
 - LsaDeleteTrustedDomain
---

# LsaDeleteTrustedDomain function


## -description

The <b>LsaDeleteTrustedDomain</b> function removes a trusted domain from the list of trusted domains for a system and deletes the associated <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param PolicyHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object. For more information, see 
<a href="/windows/desktop/SecMgmt/opening-a-policy-object-handle">Opening a Policy Object Handle</a>.

### -param TrustedDomainSid [in]

Pointer to the SID of the trusted domain to be removed.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>