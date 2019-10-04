---
UID: NS:sspi._SecPkgContext_Bindings
title: SecPkgContext_Bindings (sspi.h)
author: windows-sdk-content
description: Specifies a structure that contains channel binding information for a security context.
old-location: security\secpkgcontext_bindings.htm
tech.root: SecAuthN
ms.assetid: 6823cc31-acd3-4d67-92c6-65ff4d1c6aed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_Bindings, PSecPkgContext_Bindings, PSecPkgContext_Bindings structure pointer [Security], SecPkgContext_Bindings, SecPkgContext_Bindings structure [Security], security.secpkgcontext_bindings, sspi/PSecPkgContext_Bindings, sspi/SecPkgContext_Bindings'
ms.topic: struct
f1_keywords:
- sspi/SecPkgContext_Bindings
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Sspi.h
api_name:
- SecPkgContext_Bindings
targetos: Windows
req.typenames: SecPkgContext_Bindings, *PSecPkgContext_Bindings
req.redist: 
ms.custom: 19H1
---

# SecPkgContext_Bindings structure


## -description


Specifies a structure that contains channel binding information for a security <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a>.


## -struct-fields




### -field BindingsLength

The size, in bytes, of the structure specified by the <b>Bindings</b> member


### -field Bindings

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-sec_channel_bindings">SEC_CHANNEL_BINDINGS</a> structure that specifies channel binding information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycontextattributesw">QueryContextAttributes (Schannel)</a>
 

 

