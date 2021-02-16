---
UID: NS:sspi._SecPkgContext_CredInfo
title: SecPkgContext_CredInfo (sspi.h)
description: Specifies the type of credentials used to create a client context.
helpviewer_keywords: ["*PSecPkgContext_CredInfo","PSecPkgContext_CredInfo","PSecPkgContext_CredInfo structure pointer [Security]","SecPkgContext_CredInfo","SecPkgContext_CredInfo structure [Security]","security.secpkgcontext_credinfo","sspi/PSecPkgContext_CredInfo","sspi/SecPkgContext_CredInfo"]
old-location: security\secpkgcontext_credinfo.htm
tech.root: security
ms.assetid: 5c2c6d01-5de3-4dd1-9fa2-cce9eadd6902
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_CredInfo, PSecPkgContext_CredInfo, PSecPkgContext_CredInfo structure pointer [Security], SecPkgContext_CredInfo, SecPkgContext_CredInfo structure [Security], security.secpkgcontext_credinfo, sspi/PSecPkgContext_CredInfo, sspi/SecPkgContext_CredInfo'
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SecPkgContext_CredInfo, *PSecPkgContext_CredInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_CredInfo
 - sspi/_SecPkgContext_CredInfo
 - PSecPkgContext_CredInfo
 - sspi/PSecPkgContext_CredInfo
 - SecPkgContext_CredInfo
 - sspi/SecPkgContext_CredInfo
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
 - SecPkgContext_CredInfo
---

# SecPkgContext_CredInfo structure


## -description

Specifies the type of credentials used to create a client context.

## -struct-fields

### -field CredClass

A value of the <a href="/windows/desktop/api/sspi/ne-sspi-secpkg_cred_class">SECPKG_CRED_CLASS</a> enumeration that indicates the type of credentials.

### -field IsPromptingNeeded

A nonzero value indicates that the application must prompt the user for credentials. All other values indicate that the application does not need to prompt the user.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spquerycontextattributesfn">SpQueryContextAttributes</a>