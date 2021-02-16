---
UID: NS:sspi._SecPkgContext_Sizes
title: SecPkgContext_Sizes (sspi.h)
description: The SecPkgContext_Sizes structure indicates the sizes of important structures used in the message support functions. The QueryContextAttributes (General) function uses this structure.
helpviewer_keywords: ["*PSecPkgContext_Sizes","PSecPkgContext_Sizes","PSecPkgContext_Sizes structure pointer [Security]","SecPkgContext_Sizes","SecPkgContext_Sizes structure [Security]","_ssp_secpkgcontext_sizes","security.secpkgcontext_sizes","sspi/PSecPkgContext_Sizes","sspi/SecPkgContext_Sizes"]
old-location: security\secpkgcontext_sizes.htm
tech.root: security
ms.assetid: 46b6a155-8855-4aa0-a513-aa5b3760fcd4
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_Sizes, PSecPkgContext_Sizes, PSecPkgContext_Sizes structure pointer [Security], SecPkgContext_Sizes, SecPkgContext_Sizes structure [Security], _ssp_secpkgcontext_sizes, security.secpkgcontext_sizes, sspi/PSecPkgContext_Sizes, sspi/SecPkgContext_Sizes'
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
targetos: Windows
req.typenames: SecPkgContext_Sizes, *PSecPkgContext_Sizes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_Sizes
 - sspi/_SecPkgContext_Sizes
 - PSecPkgContext_Sizes
 - sspi/PSecPkgContext_Sizes
 - SecPkgContext_Sizes
 - sspi/SecPkgContext_Sizes
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
 - SecPkgContext_Sizes
---

# SecPkgContext_Sizes structure


## -description

The <b>SecPkgContext_Sizes</b> structure indicates the sizes of important structures used in the message support functions. The 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function uses this structure.

## -struct-fields

### -field cbMaxToken

Specifies the maximum size of the security token used in the authentication exchanges.

### -field cbMaxSignature

Specifies the maximum size of the signature created by the 
<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function. This member must be zero if <a href="/windows/desktop/SecGloss/i-gly">integrity</a> services are not requested or available.

### -field cbBlockSize

Specifies the preferred integral size of the messages. For example, eight indicates that messages should be of size zero mod eight for optimal performance. Messages other than this block size can be padded.

### -field cbSecurityTrailer

Size of the security trailer to be appended to messages. This member should be zero if the relevant services are not requested or available.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a>



<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a>