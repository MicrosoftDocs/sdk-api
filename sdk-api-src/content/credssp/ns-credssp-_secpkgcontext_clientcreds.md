---
UID: NS:credssp._SecPkgContext_ClientCreds
title: "_SecPkgContext_ClientCreds"
author: windows-sdk-content
description: Specifies client credentials when calling the QueryContextAttributes (CredSSP) function.
old-location: security\secpkgcontext_clientcreds.htm
tech.root: secauthn
ms.assetid: 85ab1bf7-a4d9-4b0e-b1e3-cb938c3183d3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSecPkgContext_ClientCreds, PSecPkgContext_ClientCreds, PSecPkgContext_ClientCreds structure pointer [Security], SecPkgContext_ClientCreds, SecPkgContext_ClientCreds structure [Security], _SecPkgContext_ClientCreds, credssp/PSecPkgContext_ClientCreds, credssp/SecPkgContext_ClientCreds, security.secpkgcontext_clientcreds"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credssp.h
api_name:
 - SecPkgContext_ClientCreds
product: Windows
targetos: Windows
req.typenames: SecPkgContext_ClientCreds, *PSecPkgContext_ClientCreds
req.redist: 
---

# _SecPkgContext_ClientCreds structure


## -description


The <b>SecPkgContext_ClientCreds</b> structure specifies client credentials when calling the <a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a> function.

This structure is supported only on the server.


## -struct-fields




### -field AuthBufferLen

The size, in characters, of the <b>AuthBuffer</b> buffer.


### -field AuthBuffer

A pointer to a buffer that represents the client credentials.


## -see-also




<a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a>
 

 

