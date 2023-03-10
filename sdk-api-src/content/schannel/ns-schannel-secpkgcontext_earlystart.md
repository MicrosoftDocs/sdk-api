---
UID: NS:schannel._SecPkgContext_EarlyStart
title: SecPkgContext_EarlyStart (schannel.h)
description: The SecPkgContext_EarlyStart structure contains information about whether to attempt to use the False Start feature in a security context.
helpviewer_keywords: ["*PSecPkgContext_EarlyStart","PSecPkgContext_EarlyStart","PSecPkgContext_EarlyStart structure pointer [Security]","SecPkgContext_EarlyStart","SecPkgContext_EarlyStart structure [Security]","SecPkgContext_EarlyStartA","SecPkgContext_EarlyStartW","_SecPkgContext_EarlyStart","schannel/PSecPkgContext_EarlyStart","schannel/SecPkgContext_EarlyStart","schannel/SecPkgContext_EarlyStartA","schannel/SecPkgContext_EarlyStartW","security.secpkgcontext_earlystart"]
old-location: security\secpkgcontext_earlystart.htm
tech.root: security
ms.assetid: 5DD5D0B9-CFFF-4743-94EC-A569D265D31F
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_EarlyStart, PSecPkgContext_EarlyStart, PSecPkgContext_EarlyStart structure pointer [Security], SecPkgContext_EarlyStart, SecPkgContext_EarlyStart structure [Security], SecPkgContext_EarlyStartA, SecPkgContext_EarlyStartW, _SecPkgContext_EarlyStart, schannel/PSecPkgContext_EarlyStart, schannel/SecPkgContext_EarlyStart, schannel/SecPkgContext_EarlyStartA, schannel/SecPkgContext_EarlyStartW, security.secpkgcontext_earlystart'
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
targetos: Windows
req.typenames: SecPkgContext_EarlyStart, *PSecPkgContext_EarlyStart
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_EarlyStart
 - schannel/_SecPkgContext_EarlyStart
 - PSecPkgContext_EarlyStart
 - schannel/PSecPkgContext_EarlyStart
 - SecPkgContext_EarlyStart
 - schannel/SecPkgContext_EarlyStart
dev_langs:
 - c++
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
---

# SecPkgContext_EarlyStart structure


## -description

The <b>SecPkgContext_EarlyStart</b> structure contains information about whether to attempt to use the False Start feature in a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. 

See  the <a href="/windows/desktop/winmsg/windows">Building a faster and more secure web</a> blog post for information on this feature.

## -struct-fields

### -field dwEarlyStartFlags

Determines whether to attempt client-side False Start. Set the value to <b>ENABLE_TLS_CLIENT_EARLY_START</b> (1) to use False Start.