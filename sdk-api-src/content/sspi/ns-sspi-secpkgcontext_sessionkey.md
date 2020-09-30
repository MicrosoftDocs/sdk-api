---
UID: NS:sspi._SecPkgContext_SessionKey
title: SecPkgContext_SessionKey (sspi.h)
description: The SecPkgContext_SessionKey structure contains information about the session key used for the security context. This structure is returned by the QueryContextAttributes (General) function.
helpviewer_keywords: ["*PSecPkgContext_SessionKey","PSecPkgContext_SessionKey","PSecPkgContext_SessionKey structure pointer [Security]","SecPkgContext_SessionKey","SecPkgContext_SessionKey structure [Security]","security.secpkgcontext_sessionkey","sspi/PSecPkgContext_SessionKey","sspi/SecPkgContext_SessionKey"]
old-location: security\secpkgcontext_sessionkey.htm
tech.root: security
ms.assetid: 88cf437e-3be0-4f12-9058-ad078deed6a1
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_SessionKey, PSecPkgContext_SessionKey, PSecPkgContext_SessionKey structure pointer [Security], SecPkgContext_SessionKey, SecPkgContext_SessionKey structure [Security], security.secpkgcontext_sessionkey, sspi/PSecPkgContext_SessionKey, sspi/SecPkgContext_SessionKey'
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
req.typenames: SecPkgContext_SessionKey, *PSecPkgContext_SessionKey
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_SessionKey
 - sspi/_SecPkgContext_SessionKey
 - PSecPkgContext_SessionKey
 - sspi/PSecPkgContext_SessionKey
 - SecPkgContext_SessionKey
 - sspi/SecPkgContext_SessionKey
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
 - SecPkgContext_SessionKey
---

# SecPkgContext_SessionKey structure


## -description

The <b>SecPkgContext_SessionKey</b> structure contains information about the session key used for the <a href="/windows/desktop/SecGloss/s-gly">security context</a>. This structure is returned by the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.

## -struct-fields

### -field SessionKeyLength

Size, in bytes, of the session key.

### -field SessionKey

The session key for the security context.