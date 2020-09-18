---
UID: NS:sspi._SecPkgContext_TargetInformation
title: SecPkgContext_TargetInformation (sspi.h)
description: Returns information about the credential used for the security context.
helpviewer_keywords: ["*PSecPkgContext_TargetInformation","PSecPkgContext_TargetInformation","PSecPkgContext_TargetInformation structure pointer [Security]","SecPkgContext_TargetInformation","SecPkgContext_TargetInformation structure [Security]","security.secpkgcontext_targetinformation","sspi/PSecPkgContext_TargetInformation","sspi/SecPkgContext_TargetInformation"]
old-location: security\secpkgcontext_targetinformation.htm
tech.root: security
ms.assetid: 8a5a6bd6-8678-4544-a631-5ee4347bc685
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_TargetInformation, PSecPkgContext_TargetInformation, PSecPkgContext_TargetInformation structure pointer [Security], SecPkgContext_TargetInformation, SecPkgContext_TargetInformation structure [Security], security.secpkgcontext_targetinformation, sspi/PSecPkgContext_TargetInformation, sspi/SecPkgContext_TargetInformation'
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
req.typenames: SecPkgContext_TargetInformation, *PSecPkgContext_TargetInformation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_TargetInformation
 - sspi/_SecPkgContext_TargetInformation
 - PSecPkgContext_TargetInformation
 - sspi/PSecPkgContext_TargetInformation
 - SecPkgContext_TargetInformation
 - sspi/SecPkgContext_TargetInformation
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
 - SecPkgContext_TargetInformation
---

# SecPkgContext_TargetInformation structure


## -description

The <b>SecPkgContext_TargetInformation</b> structure returns information about the credential used for the <a href="/windows/desktop/SecGloss/s-gly">security context</a>.  This structure is returned by the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.

## -struct-fields

### -field MarshalledTargetInfoLength

Size, in bytes, of <b>MarshalledTargetInfo</b>.

### -field MarshalledTargetInfo

Array of bytes that represent the credential, if a credential is provided by a credential manager.