---
UID: NS:sspi._SecPkgContext_ClientSpecifiedTarget
title: SecPkgContext_ClientSpecifiedTarget (sspi.h)
description: Specifies the service principal name (SPN) of the initial target when calling the QueryContextAttributes (Digest) function.
old-location: security\secpkgcontext_clientspecifiedtarget.htm
tech.root: SecAuthN
ms.assetid: 67536f69-a1fc-4f26-84dc-872635bafa3b
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget structure pointer [Security], SecPkgContext_ClientSpecifiedTarget, SecPkgContext_ClientSpecifiedTarget structure [Security], security.secpkgcontext_clientspecifiedtarget, sspi/PSecPkgContext_ClientSpecifiedTarget, sspi/SecPkgContext_ClientSpecifiedTarget'
ms.topic: struct
f1_keywords:
- sspi/SecPkgContext_ClientSpecifiedTarget
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
- SecPkgContext_ClientSpecifiedTarget
targetos: Windows
req.typenames: SecPkgContext_ClientSpecifiedTarget, *PSecPkgContext_ClientSpecifiedTarget
req.redist: 
ms.custom: 19H1
---

# SecPkgContext_ClientSpecifiedTarget structure


## -description


The <b>SecPkgContext_ClientSpecifiedTarget</b> structure specifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN) of the initial target when calling the <a href="https://docs.microsoft.com/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a> function.


## -struct-fields




### -field sTargetName

The SPN of the initial target.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a>
 

 

