---
UID: NS:sspi._SecPkgContext_ProtoInfoW
title: SecPkgContext_ProtoInfoW (sspi.h)
description: The SecPkgContext_ProtoInfo structure holds information about the protocol in use. (Unicode)
helpviewer_keywords: ["*PSecPkgContext_ProtoInfoW","PSecPkgContext_ProtoInfo","PSecPkgContext_ProtoInfo structure pointer [Security]","SecPkgContext_ProtoInfo","SecPkgContext_ProtoInfo structure [Security]","SecPkgContext_ProtoInfoA","SecPkgContext_ProtoInfoW","_ssp_secpkgcontext_protoinfo","security.secpkgcontext_protoinfo","sspi/PSecPkgContext_ProtoInfo","sspi/SecPkgContext_ProtoInfo"]
old-location: security\secpkgcontext_protoinfo.htm
tech.root: security
ms.assetid: c10eb1fc-b957-4853-86c1-070749488bb9
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_ProtoInfoW, PSecPkgContext_ProtoInfo, PSecPkgContext_ProtoInfo structure pointer [Security], SecPkgContext_ProtoInfo, SecPkgContext_ProtoInfo structure [Security], SecPkgContext_ProtoInfoA, SecPkgContext_ProtoInfoW, _ssp_secpkgcontext_protoinfo, security.secpkgcontext_protoinfo, sspi/PSecPkgContext_ProtoInfo, sspi/SecPkgContext_ProtoInfo'
req.header: sspi.h
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
req.typenames: SecPkgContext_ProtoInfoW, *PSecPkgContext_ProtoInfoW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_ProtoInfoW
 - sspi/_SecPkgContext_ProtoInfoW
 - PSecPkgContext_ProtoInfoW
 - sspi/PSecPkgContext_ProtoInfoW
 - SecPkgContext_ProtoInfoW
 - sspi/SecPkgContext_ProtoInfoW
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
 - SecPkgContext_ProtoInfo
---

# SecPkgContext_ProtoInfoW structure


## -description

<p class="CCE_Message">[The <b>SecPkgContext_ProtoInfo</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/api/schannel/ns-schannel-secpkgcontext_connectioninfo">SecPkgContext_ConnectionInfo</a> structure.]

The <b>SecPkgContext_ProtoInfo</b> structure holds information about the protocol in use.

This attribute is supported only by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

## -struct-fields

### -field sProtocolName

Pointer to a string containing the name of the protocol.

### -field majorVersion

Major version number.

### -field minorVersion

Minor version number.

## -remarks

> [!NOTE]
> The sspi.h header defines SecPkgContext_ProtoInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
