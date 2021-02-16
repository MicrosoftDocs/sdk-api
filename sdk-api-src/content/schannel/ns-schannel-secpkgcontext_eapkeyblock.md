---
UID: NS:schannel._SecPkgContext_EapKeyBlock
title: SecPkgContext_EapKeyBlock (schannel.h)
description: Contains key data used by the EAP TLS Authentication Protocol.
helpviewer_keywords: ["*PSecPkgContext_EapKeyBlock","PSecPkgContext_EapKeyBlock","PSecPkgContext_EapKeyBlock structure pointer [Security]","SecPkgContext_EapKeyBlock","SecPkgContext_EapKeyBlock structure [Security]","schannel/PSecPkgContext_EapKeyBlock","schannel/SecPkgContext_EapKeyBlock","security.secpkgcontext_eapkeyblock"]
old-location: security\secpkgcontext_eapkeyblock.htm
tech.root: security
ms.assetid: c1b1f1d1-20f9-4a16-a279-b9cc95ff4e64
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_EapKeyBlock, PSecPkgContext_EapKeyBlock, PSecPkgContext_EapKeyBlock structure pointer [Security], SecPkgContext_EapKeyBlock, SecPkgContext_EapKeyBlock structure [Security], schannel/PSecPkgContext_EapKeyBlock, schannel/SecPkgContext_EapKeyBlock, security.secpkgcontext_eapkeyblock'
req.header: schannel.h
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
req.typenames: SecPkgContext_EapKeyBlock, *PSecPkgContext_EapKeyBlock
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_EapKeyBlock
 - schannel/_SecPkgContext_EapKeyBlock
 - PSecPkgContext_EapKeyBlock
 - schannel/PSecPkgContext_EapKeyBlock
 - SecPkgContext_EapKeyBlock
 - schannel/SecPkgContext_EapKeyBlock
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
 - SecPkgContext_EapKeyBlock
---

# SecPkgContext_EapKeyBlock structure


## -description

The <b>SecPkgContext_EapKeyBlock</b> structure contains key data used by the EAP TLS Authentication Protocol. For information about the EAP TLS Authentication Protocol, see <a href="https://www.ietf.org/rfc/rfc2716.txt">http://www.ietf.org/rfc/rfc2716.txt</a>.

## -struct-fields

### -field rgbKeys

An array of 128 bytes that contain key data used by the EAP TLS Authentication Protocol.

### -field rgbIVs

An array of 64 bytes that contain initialization vector data used by the EAP TLS Authentication Protocol.

