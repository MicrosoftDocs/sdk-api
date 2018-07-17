---
UID: NS:schannel._SecPkgContext_EapKeyBlock
title: "_SecPkgContext_EapKeyBlock"
author: windows-sdk-content
description: Contains key data used by the EAP TLS Authentication Protocol.
old-location: security\secpkgcontext_eapkeyblock.htm
old-project: secauthn
ms.assetid: c1b1f1d1-20f9-4a16-a279-b9cc95ff4e64
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "*PSecPkgContext_EapKeyBlock, PSecPkgContext_EapKeyBlock, PSecPkgContext_EapKeyBlock structure pointer [Security], SecPkgContext_EapKeyBlock, SecPkgContext_EapKeyBlock structure [Security], _SecPkgContext_EapKeyBlock, schannel/PSecPkgContext_EapKeyBlock, schannel/SecPkgContext_EapKeyBlock, security.secpkgcontext_eapkeyblock"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SecPkgContext_EapKeyBlock, *PSecPkgContext_EapKeyBlock
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SecPkgContext_EapKeyBlock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SecPkgContext_EapKeyBlock structure


## -description


The <b>SecPkgContext_EapKeyBlock</b> structure contains key data used by the EAP TLS Authentication Protocol. For information about the EAP TLS Authentication Protocol, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84050">http://www.ietf.org/rfc/rfc2716.txt</a>.


## -struct-fields




### -field rgbKeys

An array of 128 bytes that contain key data used by the EAP TLS Authentication Protocol.


### -field rgbIVs

An array of 64 bytes that contain initialization vector data used by the EAP TLS Authentication Protocol.

