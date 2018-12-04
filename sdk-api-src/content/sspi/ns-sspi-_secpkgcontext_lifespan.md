---
UID: NS:sspi._SecPkgContext_Lifespan
title: "_SecPkgContext_Lifespan"
author: windows-sdk-content
description: The SecPkgContext_Lifespan structure indicates the life span of a security context. The QueryContextAttributes (General) function uses this structure.
old-location: security\secpkgcontext_lifespan.htm
tech.root: secauthn
ms.assetid: 7ef45795-f6af-4dac-a498-c6f8c915a168
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PSecPkgContext_Lifespan, PSecPkgContext_Lifespan, PSecPkgContext_Lifespan structure pointer [Security], SecPkgContext_Lifespan, SecPkgContext_Lifespan structure [Security], _SecPkgContext_Lifespan, _ssp_secpkgcontext_lifespan, security.secpkgcontext_lifespan, sspi/PSecPkgContext_Lifespan, sspi/SecPkgContext_Lifespan"
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
 - SecPkgContext_Lifespan
product: Windows
targetos: Windows
req.typenames: SecPkgContext_Lifespan, *PSecPkgContext_Lifespan
req.redist: 
---

# _SecPkgContext_Lifespan structure


## -description


The <b>SecPkgContext_Lifespan</b> structure indicates the life span of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.


## -struct-fields




### -field tsStart

Time at which the context was established.


### -field tsExpiry

Time at which the context will expire.


## -remarks



It is recommended that the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> always return these values in local time.




## -see-also




<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes</a>
 

 

