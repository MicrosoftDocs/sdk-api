---
UID: NS:credssp._SecPkgContext_ClientCreds
title: SecPkgContext_ClientCreds (credssp.h)
description: Specifies client credentials when calling the QueryContextAttributes (CredSSP) function.
helpviewer_keywords: ["*PSecPkgContext_ClientCreds","PSecPkgContext_ClientCreds","PSecPkgContext_ClientCreds structure pointer [Security]","SecPkgContext_ClientCreds","SecPkgContext_ClientCreds structure [Security]","credssp/PSecPkgContext_ClientCreds","credssp/SecPkgContext_ClientCreds","security.secpkgcontext_clientcreds"]
old-location: security\secpkgcontext_clientcreds.htm
tech.root: security
ms.assetid: 85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_ClientCreds, PSecPkgContext_ClientCreds, PSecPkgContext_ClientCreds structure pointer [Security], SecPkgContext_ClientCreds, SecPkgContext_ClientCreds structure [Security], credssp/PSecPkgContext_ClientCreds, credssp/SecPkgContext_ClientCreds, security.secpkgcontext_clientcreds'
req.header: credssp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SecPkgContext_ClientCreds, *PSecPkgContext_ClientCreds
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_ClientCreds
 - credssp/_SecPkgContext_ClientCreds
 - PSecPkgContext_ClientCreds
 - credssp/PSecPkgContext_ClientCreds
 - SecPkgContext_ClientCreds
 - credssp/SecPkgContext_ClientCreds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credssp.h
api_name:
 - SecPkgContext_ClientCreds
---

# SecPkgContext_ClientCreds structure


## -description

The <b>SecPkgContext_ClientCreds</b> structure specifies client credentials when calling the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (CredSSP)</a> function.

This structure is supported only on the server.

## -struct-fields

### -field AuthBufferLen

The size, in characters, of the <b>AuthBuffer</b> buffer.

### -field AuthBuffer

A pointer to a buffer that represents the client credentials.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (CredSSP)</a>