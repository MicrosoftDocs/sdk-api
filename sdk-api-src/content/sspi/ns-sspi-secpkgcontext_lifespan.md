---
UID: NS:sspi._SecPkgContext_Lifespan
title: SecPkgContext_Lifespan (sspi.h)
description: The SecPkgContext_Lifespan structure indicates the life span of a security context. The QueryContextAttributes (General) function uses this structure.
helpviewer_keywords: ["*PSecPkgContext_Lifespan","PSecPkgContext_Lifespan","PSecPkgContext_Lifespan structure pointer [Security]","SecPkgContext_Lifespan","SecPkgContext_Lifespan structure [Security]","_ssp_secpkgcontext_lifespan","security.secpkgcontext_lifespan","sspi/PSecPkgContext_Lifespan","sspi/SecPkgContext_Lifespan"]
old-location: security\secpkgcontext_lifespan.htm
tech.root: security
ms.assetid: 7ef45795-f6af-4dac-a498-c6f8c915a168
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_Lifespan, PSecPkgContext_Lifespan, PSecPkgContext_Lifespan structure pointer [Security], SecPkgContext_Lifespan, SecPkgContext_Lifespan structure [Security], _ssp_secpkgcontext_lifespan, security.secpkgcontext_lifespan, sspi/PSecPkgContext_Lifespan, sspi/SecPkgContext_Lifespan'
req.header: sspi.h
req.include-header: Security.h
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
req.typenames: SecPkgContext_Lifespan, *PSecPkgContext_Lifespan
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_Lifespan
 - sspi/_SecPkgContext_Lifespan
 - PSecPkgContext_Lifespan
 - sspi/PSecPkgContext_Lifespan
 - SecPkgContext_Lifespan
 - sspi/SecPkgContext_Lifespan
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
 - SecPkgContext_Lifespan
---

# SecPkgContext_Lifespan structure


## -description

The <b>SecPkgContext_Lifespan</b> structure indicates the life span of a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

## -struct-fields

### -field tsStart

Time at which the context was established.

### -field tsExpiry

Time at which the context will expire.

## -remarks

It is recommended that the <a href="/windows/desktop/SecGloss/s-gly">security package</a> always return these values in local time.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes</a>