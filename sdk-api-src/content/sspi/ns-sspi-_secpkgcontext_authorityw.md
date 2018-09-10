---
UID: NS:sspi._SecPkgContext_AuthorityW
title: "_SecPkgContext_AuthorityW"
author: windows-sdk-content
description: The SecPkgContext_Authority structure contains the name of the authenticating authority if one is available.
old-location: security\secpkgcontext_authority.htm
tech.root: SecAuthN
ms.assetid: 619bf16b-c439-48e7-b013-3622e2f3bbc4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSecPkgContext_AuthorityW, PSecPkgContext_Authority, PSecPkgContext_Authority structure pointer [Security], SecPkgContext_Authority, SecPkgContext_Authority structure [Security], SecPkgContext_AuthorityA, SecPkgContext_AuthorityW, _SecPkgContext_AuthorityW, _ssp_secpkgcontext_authority, security.secpkgcontext_authority, sspi/PSecPkgContext_Authority, sspi/SecPkgContext_Authority, sspi/SecPkgContext_AuthorityA, sspi/SecPkgContext_AuthorityW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_AuthorityW (Unicode) and SecPkgContext_AuthorityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_Authority
 - SecPkgContext_AuthorityA
 - SecPkgContext_AuthorityW
product: Windows
targetos: Windows
req.typenames: SecPkgContext_AuthorityW, *PSecPkgContext_AuthorityW
req.redist: 
---

# _SecPkgContext_AuthorityW structure


## -description


The <b>SecPkgContext_Authority</b> structure contains the name of the authenticating authority if one is available. It can be a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) or the name of a server or domain that authenticated the connection. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.
		


## -struct-fields




### -field sAuthorityName

Pointer to a null-terminated string containing the name of the authenticating authority, if available.

