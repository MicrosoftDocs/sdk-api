---
UID: NS:sspi._SecPkgContext_NamesA
title: SecPkgContext_NamesA (sspi.h)
description: The SecPkgContext_Names structure indicates the name of the user associated with a security context. The QueryContextAttributes (General) function uses this structure. (ANSI)
helpviewer_keywords: ["*PSecPkgContext_NamesA","SecPkgContext_Names","SecPkgContext_Names structure [Security]","SecPkgContext_NamesA","SecPkgContext_NamesW","_ssp_secpkgcontext_names","pSecPkgContext_Names","pSecPkgContext_Names structure pointer [Security]","security.secpkgcontext_names","sspi/SecPkgContext_Names","sspi/SecPkgContext_NamesA","sspi/SecPkgContext_NamesW","sspi/pSecPkgContext_Names"]
old-location: security\secpkgcontext_names.htm
tech.root: security
ms.assetid: 9df0bf7c-ad5f-4cb8-8934-76062789735f
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_NamesA, SecPkgContext_Names, SecPkgContext_Names structure [Security], SecPkgContext_NamesA, SecPkgContext_NamesW, _ssp_secpkgcontext_names, pSecPkgContext_Names, pSecPkgContext_Names structure pointer [Security], security.secpkgcontext_names, sspi/SecPkgContext_Names, sspi/SecPkgContext_NamesA, sspi/SecPkgContext_NamesW, sspi/pSecPkgContext_Names'
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_NamesW (Unicode) and SecPkgContext_NamesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_NamesA, *PSecPkgContext_NamesA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_NamesA
 - sspi/_SecPkgContext_NamesA
 - PSecPkgContext_NamesA
 - sspi/PSecPkgContext_NamesA
 - SecPkgContext_NamesA
 - sspi/SecPkgContext_NamesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_Names
 - SecPkgContext_NamesA
 - SecPkgContext_NamesW
---

# SecPkgContext_NamesA structure


## -description

The <b>SecPkgContext_Names</b> structure indicates the name of the user associated with a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

## -struct-fields

### -field sUserName

Pointer to a null-terminated string containing the name of the user represented by the context. If the <a href="/windows/desktop/SecGloss/s-gly">security package</a> has set the SECPKG_FLAG_ACCEPT_WIN32_NAME flag, this name can be used in other Windows calls.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgContext_Names as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
