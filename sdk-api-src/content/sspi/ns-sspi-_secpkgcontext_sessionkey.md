---
UID: NS:sspi._SecPkgContext_SessionKey
title: "_SecPkgContext_SessionKey"
author: windows-sdk-content
description: The SecPkgContext_SessionKey structure contains information about the session key used for the security context. This structure is returned by the QueryContextAttributes (General) function.
old-location: security\secpkgcontext_sessionkey.htm
tech.root: secauthn
ms.assetid: 88cf437e-3be0-4f12-9058-ad078deed6a1
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PSecPkgContext_SessionKey, PSecPkgContext_SessionKey, PSecPkgContext_SessionKey structure pointer [Security], SecPkgContext_SessionKey, SecPkgContext_SessionKey structure [Security], _SecPkgContext_SessionKey, security.secpkgcontext_sessionkey, sspi/PSecPkgContext_SessionKey, sspi/SecPkgContext_SessionKey"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_SessionKey
product: Windows
targetos: Windows
req.typenames: SecPkgContext_SessionKey, *PSecPkgContext_SessionKey
req.redist: 
---

# _SecPkgContext_SessionKey structure


## -description


The <b>SecPkgContext_SessionKey</b> structure contains information about the session key used for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. This structure is returned by the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


## -struct-fields




### -field SessionKeyLength

Size, in bytes, of the session key.


### -field SessionKey

The session key for the security context.

