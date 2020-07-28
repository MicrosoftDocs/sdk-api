---
UID: NS:sspi._SecPkgContext_AuthorityW
title: SecPkgContext_AuthorityW (sspi.h)
description: The SecPkgContext_Authority structure contains the name of the authenticating authority if one is available.
helpviewer_keywords: ["*PSecPkgContext_AuthorityW","PSecPkgContext_Authority","PSecPkgContext_Authority structure pointer [Security]","SecPkgContext_Authority","SecPkgContext_Authority structure [Security]","SecPkgContext_AuthorityA","SecPkgContext_AuthorityW","_ssp_secpkgcontext_authority","security.secpkgcontext_authority","sspi/PSecPkgContext_Authority","sspi/SecPkgContext_Authority","sspi/SecPkgContext_AuthorityA","sspi/SecPkgContext_AuthorityW"]
old-location: security\secpkgcontext_authority.htm
tech.root: security
ms.assetid: 619bf16b-c439-48e7-b013-3622e2f3bbc4
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_AuthorityW, PSecPkgContext_Authority, PSecPkgContext_Authority structure pointer [Security], SecPkgContext_Authority, SecPkgContext_Authority structure [Security], SecPkgContext_AuthorityA, SecPkgContext_AuthorityW, _ssp_secpkgcontext_authority, security.secpkgcontext_authority, sspi/PSecPkgContext_Authority, sspi/SecPkgContext_Authority, sspi/SecPkgContext_AuthorityA, sspi/SecPkgContext_AuthorityW'
f1_keywords:
- sspi/SecPkgContext_Authority
dev_langs:
- c++
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_AuthorityW (Unicode) and SecPkgContext_AuthorityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Sspi.h
api_name:
- SecPkgContext_Authority
- SecPkgContext_AuthorityA
- SecPkgContext_AuthorityW
targetos: Windows
req.typenames: SecPkgContext_AuthorityW, *PSecPkgContext_AuthorityW
req.redist: 
ms.custom: 19H1
---

# SecPkgContext_AuthorityW structure


## -description


The <b>SecPkgContext_Authority</b> structure contains the name of the authenticating authority if one is available. It can be a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) or the name of a server or domain that authenticated the connection. The 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.
		


## -struct-fields




### -field sAuthorityName

Pointer to a null-terminated string containing the name of the authenticating authority, if available.

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgContext_Authority as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

