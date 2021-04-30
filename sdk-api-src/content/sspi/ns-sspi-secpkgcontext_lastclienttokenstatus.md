---
UID: NS:sspi._SecPkgContext_LastClientTokenStatus
title: SecPkgContext_LastClientTokenStatus (sspi.h)
description: Specifies whether the token from the most recent call to the InitializeSecurityContext function is the last token from the client.
helpviewer_keywords: ["*PSecPkgContext_LastClientTokenStatus","PSecPkgContext_LastClientTokenStatus","PSecPkgContext_LastClientTokenStatus structure pointer [Security]","SecPkgContext_LastClientTokenStatus","SecPkgContext_LastClientTokenStatus structure [Security]","security.secpkgcontext_lastclienttokenstatus","sspi/PSecPkgContext_LastClientTokenStatus","sspi/SecPkgContext_LastClientTokenStatus"]
old-location: security\secpkgcontext_lastclienttokenstatus.htm
tech.root: security
ms.assetid: ccb2bb4e-3c65-4305-95ad-b9111f3936b5
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_LastClientTokenStatus, PSecPkgContext_LastClientTokenStatus, PSecPkgContext_LastClientTokenStatus structure pointer [Security], SecPkgContext_LastClientTokenStatus, SecPkgContext_LastClientTokenStatus structure [Security], security.secpkgcontext_lastclienttokenstatus, sspi/PSecPkgContext_LastClientTokenStatus, sspi/SecPkgContext_LastClientTokenStatus'
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
req.typenames: SecPkgContext_LastClientTokenStatus, *PSecPkgContext_LastClientTokenStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_LastClientTokenStatus
 - sspi/_SecPkgContext_LastClientTokenStatus
 - PSecPkgContext_LastClientTokenStatus
 - sspi/PSecPkgContext_LastClientTokenStatus
 - SecPkgContext_LastClientTokenStatus
 - sspi/SecPkgContext_LastClientTokenStatus
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
 - SecPkgContext_LastClientTokenStatus
---

# SecPkgContext_LastClientTokenStatus structure


## -description

Specifies whether the token from the most recent call to the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> function is the last token from the client.

## -struct-fields

### -field LastClientTokenStatus

A value of the <a href="/windows/desktop/api/sspi/ne-sspi-secpkg_attr_lct_status">SECPKG_ATTR_LCT_STATUS</a> enumeration that indicates the status of the token returned by the most recent  call to <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a>.

## -see-also

<a href="/windows/desktop/api/sspi/ne-sspi-secpkg_attr_lct_status">SECPKG_ATTR_LCT_STATUS</a>