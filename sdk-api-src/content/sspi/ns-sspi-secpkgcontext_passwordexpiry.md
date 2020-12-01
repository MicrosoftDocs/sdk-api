---
UID: NS:sspi._SecPkgContext_PasswordExpiry
title: SecPkgContext_PasswordExpiry (sspi.h)
description: The SecPkgContext_PasswordExpiry structure contains information about the expiration of a password or other credential used for the security context. This structure is returned by QueryContextAttributes (General).
helpviewer_keywords: ["*PSecPkgContext_PasswordExpiry","PSecPkgContext_PasswordExpiry","PSecPkgContext_PasswordExpiry structure pointer [Security]","SecPkgContext_PasswordExpiry","SecPkgContext_PasswordExpiry structure [Security]","security.secpkgcontext_passwordexpiry","sspi/PSecPkgContext_PasswordExpiry","sspi/SecPkgContext_PasswordExpiry"]
old-location: security\secpkgcontext_passwordexpiry.htm
tech.root: security
ms.assetid: f45dde88-1520-4e65-8fae-8407dfaa0850
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_PasswordExpiry, PSecPkgContext_PasswordExpiry, PSecPkgContext_PasswordExpiry structure pointer [Security], SecPkgContext_PasswordExpiry, SecPkgContext_PasswordExpiry structure [Security], security.secpkgcontext_passwordexpiry, sspi/PSecPkgContext_PasswordExpiry, sspi/SecPkgContext_PasswordExpiry'
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
req.typenames: SecPkgContext_PasswordExpiry, *PSecPkgContext_PasswordExpiry
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_PasswordExpiry
 - sspi/_SecPkgContext_PasswordExpiry
 - PSecPkgContext_PasswordExpiry
 - sspi/PSecPkgContext_PasswordExpiry
 - SecPkgContext_PasswordExpiry
 - sspi/SecPkgContext_PasswordExpiry
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
 - SecPkgContext_PasswordExpiry
---

# SecPkgContext_PasswordExpiry structure


## -description

The <b>SecPkgContext_PasswordExpiry</b> structure contains information about the expiration of a password or other credential used for the <a href="/windows/desktop/SecGloss/s-gly">security context</a>. This structure is returned by <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>.

## -struct-fields

### -field tsPasswordExpires

A <a href="/windows/desktop/SecAuthN/timestamp">TimeStamp</a> variable that indicates when the credentials for the security context expire. For password-based packages, this variable indicates when the password expires. For <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a>, this variable indicates when the ticket expires.