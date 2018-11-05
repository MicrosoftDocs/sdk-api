---
UID: NS:schannel._SecPkgContext_EarlyStart
title: "_SecPkgContext_EarlyStart"
author: windows-sdk-content
description: The SecPkgContext_EarlyStart structure contains information about whether to attempt to use the False Start feature in a security context.
old-location: security\secpkgcontext_earlystart.htm
tech.root: secauthn
ms.assetid: 5DD5D0B9-CFFF-4743-94EC-A569D265D31F
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PSecPkgContext_EarlyStart, PSecPkgContext_EarlyStart, PSecPkgContext_EarlyStart structure pointer [Security], SecPkgContext_EarlyStart, SecPkgContext_EarlyStart structure [Security], SecPkgContext_EarlyStartA, SecPkgContext_EarlyStartW, _SecPkgContext_EarlyStart, schannel/PSecPkgContext_EarlyStart, schannel/SecPkgContext_EarlyStart, schannel/SecPkgContext_EarlyStartA, schannel/SecPkgContext_EarlyStartW, security.secpkgcontext_earlystart"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_EarlyStartW (Unicode) and SecPkgContext_EarlyStartA (ANSI)
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
 - schannel.h
api_name:
 - SecPkgContext_EarlyStart
 - SecPkgContext_EarlyStartA
 - SecPkgContext_EarlyStartW
product: Windows
targetos: Windows
req.typenames: SecPkgContext_EarlyStart, *PSecPkgContext_EarlyStart
req.redist: 
---

# _SecPkgContext_EarlyStart structure


## -description


The <b>SecPkgContext_EarlyStart</b> structure contains information about whether to attempt to use the False Start feature in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. 

See  the <a href="https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/">Building a faster and more secure web</a> blog post for information on this feature.


## -struct-fields




### -field dwEarlyStartFlags

Determines whether to attempt client-side False Start. Set the value to <b>ENABLE_TLS_CLIENT_EARLY_START</b> (1) to use False Start. 

