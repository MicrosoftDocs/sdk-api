---
UID: NS:sspi._SecPkgContext_Bindings
title: "_SecPkgContext_Bindings"
author: windows-sdk-content
description: Specifies a structure that contains channel binding information for a security context.
old-location: security\secpkgcontext_bindings.htm
tech.root: secauthn
ms.assetid: 6823cc31-acd3-4d67-92c6-65ff4d1c6aed
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PSecPkgContext_Bindings, PSecPkgContext_Bindings, PSecPkgContext_Bindings structure pointer [Security], SecPkgContext_Bindings, SecPkgContext_Bindings structure [Security], _SecPkgContext_Bindings, security.secpkgcontext_bindings, sspi/PSecPkgContext_Bindings, sspi/SecPkgContext_Bindings"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SecPkgContext_Bindings, *PSecPkgContext_Bindings
req.redist: 
---

# _SecPkgContext_Bindings structure


## -description


Specifies a structure that contains channel binding information for a security <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.


## -struct-fields




### -field BindingsLength

The size, in bytes, of the structure specified by the <b>Bindings</b> member


### -field Bindings

A pointer to a <a href="https://msdn.microsoft.com/1cdbe53f-3fa0-46b1-9449-8fd3db6cddce">SEC_CHANNEL_BINDINGS</a> structure that specifies channel binding information.


## -see-also




<a href="https://msdn.microsoft.com/0329e525-a743-4e6c-aac4-9f74274dadd2">QueryContextAttributes (Schannel)</a>
 

 

