---
UID: NS:schannel._SecPkgContext_SessionAppData
title: SecPkgContext_SessionAppData (schannel.h)
description: Stores application data for a session context.
helpviewer_keywords: ["*PSecPkgContext_SessionAppData","SecPkgContext_SessionAppData","SecPkgContext_SessionAppData structure [Security]","schannel/SecPkgContext_SessionAppData","security.secpkgcontext_sessionappdata"]
old-location: security\secpkgcontext_sessionappdata.htm
tech.root: security
ms.assetid: 7bda791a-dd60-4651-bfe8-13333017d6a3
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_SessionAppData, SecPkgContext_SessionAppData, SecPkgContext_SessionAppData structure [Security], schannel/SecPkgContext_SessionAppData, security.secpkgcontext_sessionappdata'
req.header: schannel.h
req.include-header: Schnlsp.h
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
req.typenames: SecPkgContext_SessionAppData, *PSecPkgContext_SessionAppData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_SessionAppData
 - schannel/_SecPkgContext_SessionAppData
 - PSecPkgContext_SessionAppData
 - schannel/PSecPkgContext_SessionAppData
 - SecPkgContext_SessionAppData
 - schannel/SecPkgContext_SessionAppData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SecPkgContext_SessionAppData
---

# SecPkgContext_SessionAppData structure


## -description

The <b>SecPkgContext_SessionAppData</b> structure stores application data for a session context.

This attribute is supported only by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

## -struct-fields

### -field dwFlags

Reserved for future use.

### -field cbAppData

Count of bytes used by <b>pbAppData</b>.

### -field pbAppData

Pointer to a <b>BYTE</b> that represents the session application data.