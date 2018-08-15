---
UID: NS:sspi._SecPkgContext_PasswordExpiry
title: "_SecPkgContext_PasswordExpiry"
author: windows-sdk-content
description: The SecPkgContext_PasswordExpiry structure contains information about the expiration of a password or other credential used for the security context. This structure is returned by QueryContextAttributes (General).
old-location: security\secpkgcontext_passwordexpiry.htm
old-project: secauthn
ms.assetid: f45dde88-1520-4e65-8fae-8407dfaa0850
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSecPkgContext_PasswordExpiry, PSecPkgContext_PasswordExpiry, PSecPkgContext_PasswordExpiry structure pointer [Security], SecPkgContext_PasswordExpiry, SecPkgContext_PasswordExpiry structure [Security], _SecPkgContext_PasswordExpiry, security.secpkgcontext_passwordexpiry, sspi/PSecPkgContext_PasswordExpiry, sspi/SecPkgContext_PasswordExpiry"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.redist: 
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
tech.root: 
req.typenames: SecPkgContext_PasswordExpiry, *PSecPkgContext_PasswordExpiry
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_PasswordExpiry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_PasswordExpiry structure


## -description


The <b>SecPkgContext_PasswordExpiry</b> structure contains information about the expiration of a password or other credential used for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. This structure is returned by <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>.


## -struct-fields




### -field tsPasswordExpires

A <a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> variable that indicates when the credentials for the security context expire. For password-based packages, this variable indicates when the password expires. For <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a>, this variable indicates when the ticket expires.

