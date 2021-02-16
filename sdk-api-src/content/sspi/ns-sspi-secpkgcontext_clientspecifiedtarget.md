---
UID: NS:sspi._SecPkgContext_ClientSpecifiedTarget
title: SecPkgContext_ClientSpecifiedTarget (sspi.h)
description: Specifies the service principal name (SPN) of the initial target when calling the QueryContextAttributes (Digest) function.
helpviewer_keywords: ["*PSecPkgContext_ClientSpecifiedTarget","PSecPkgContext_ClientSpecifiedTarget","PSecPkgContext_ClientSpecifiedTarget structure pointer [Security]","SecPkgContext_ClientSpecifiedTarget","SecPkgContext_ClientSpecifiedTarget structure [Security]","security.secpkgcontext_clientspecifiedtarget","sspi/PSecPkgContext_ClientSpecifiedTarget","sspi/SecPkgContext_ClientSpecifiedTarget"]
old-location: security\secpkgcontext_clientspecifiedtarget.htm
tech.root: security
ms.assetid: 67536f69-a1fc-4f26-84dc-872635bafa3b
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget, PSecPkgContext_ClientSpecifiedTarget structure pointer [Security], SecPkgContext_ClientSpecifiedTarget, SecPkgContext_ClientSpecifiedTarget structure [Security], security.secpkgcontext_clientspecifiedtarget, sspi/PSecPkgContext_ClientSpecifiedTarget, sspi/SecPkgContext_ClientSpecifiedTarget'
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
targetos: Windows
req.typenames: SecPkgContext_ClientSpecifiedTarget, *PSecPkgContext_ClientSpecifiedTarget
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_ClientSpecifiedTarget
 - sspi/_SecPkgContext_ClientSpecifiedTarget
 - PSecPkgContext_ClientSpecifiedTarget
 - sspi/PSecPkgContext_ClientSpecifiedTarget
 - SecPkgContext_ClientSpecifiedTarget
 - sspi/SecPkgContext_ClientSpecifiedTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_ClientSpecifiedTarget
---

# SecPkgContext_ClientSpecifiedTarget structure


## -description

The <b>SecPkgContext_ClientSpecifiedTarget</b> structure specifies the <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN) of the initial target when calling the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a> function.

## -struct-fields

### -field sTargetName

The SPN of the initial target.

## -see-also

<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a>