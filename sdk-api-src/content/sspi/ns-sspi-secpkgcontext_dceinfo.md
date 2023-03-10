---
UID: NS:sspi._SecPkgContext_DceInfo
title: SecPkgContext_DceInfo (sspi.h)
description: The SecPkgContext_DceInfo structure contains authorization data used by DCE services. The QueryContextAttributes (General) function uses this structure.
helpviewer_keywords: ["*PSecPkgContext_DceInfo","PSecPkgContext_DceInfo","PSecPkgContext_DceInfo structure pointer [Security]","SecPkgContext_DceInfo","SecPkgContext_DceInfo structure [Security]","_ssp_secpkgcontext_dceinfo","security.secpkgcontext_dceinfo","sspi/PSecPkgContext_DceInfo","sspi/SecPkgContext_DceInfo"]
old-location: security\secpkgcontext_dceinfo.htm
tech.root: security
ms.assetid: 490688d0-efdd-4a40-88b9-eb53ff592d2a
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_DceInfo, PSecPkgContext_DceInfo, PSecPkgContext_DceInfo structure pointer [Security], SecPkgContext_DceInfo, SecPkgContext_DceInfo structure [Security], _ssp_secpkgcontext_dceinfo, security.secpkgcontext_dceinfo, sspi/PSecPkgContext_DceInfo, sspi/SecPkgContext_DceInfo'
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
req.typenames: SecPkgContext_DceInfo, *PSecPkgContext_DceInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_DceInfo
 - sspi/_SecPkgContext_DceInfo
 - PSecPkgContext_DceInfo
 - sspi/PSecPkgContext_DceInfo
 - SecPkgContext_DceInfo
 - sspi/SecPkgContext_DceInfo
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
 - SecPkgContext_DceInfo
---

# SecPkgContext_DceInfo structure


## -description

The <b>SecPkgContext_DceInfo</b> structure contains authorization data used by DCE services. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

## -struct-fields

### -field AuthzSvc

Specifies the authorization service used. For DCE use only.

### -field pPac

Pointer to package-specific authorization data.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>