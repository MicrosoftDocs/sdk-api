---
UID: NS:sspi._SecPkgContext_Flags
title: SecPkgContext_Flags (sspi.h)
description: The SecPkgContext_Flags structure contains information about the flags in the current security context. This structure is returned by QueryContextAttributes (General).
helpviewer_keywords: ["*PSecPkgContext_Flags","PSecPkgContext_Flags","PSecPkgContext_Flags structure pointer [Security]","SecPkgContext_Flags","SecPkgContext_Flags structure [Security]","security.secpkgcontext_flags","sspi/PSecPkgContext_Flags","sspi/SecPkgContext_Flags"]
old-location: security\secpkgcontext_flags.htm
tech.root: security
ms.assetid: 0be0e945-4048-4748-a9fd-15d08fb7ff3e
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_Flags, PSecPkgContext_Flags, PSecPkgContext_Flags structure pointer [Security], SecPkgContext_Flags, SecPkgContext_Flags structure [Security], security.secpkgcontext_flags, sspi/PSecPkgContext_Flags, sspi/SecPkgContext_Flags'
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
req.typenames: SecPkgContext_Flags, *PSecPkgContext_Flags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_Flags
 - sspi/_SecPkgContext_Flags
 - PSecPkgContext_Flags
 - sspi/PSecPkgContext_Flags
 - SecPkgContext_Flags
 - sspi/SecPkgContext_Flags
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
 - SecPkgContext_Flags
---

# SecPkgContext_Flags structure


## -description

The <b>SecPkgContext_Flags</b> structure contains information about the flags in the current <a href="/windows/desktop/SecGloss/s-gly">security context</a>. This structure is returned by <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>.

## -struct-fields

### -field Flags

Flag values for the current security context. These values correspond to the flags negotiated by the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> and <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> functions.