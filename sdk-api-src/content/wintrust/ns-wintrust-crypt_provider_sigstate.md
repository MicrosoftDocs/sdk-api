---
UID: NS:wintrust._CRYPT_PROVIDER_SIGSTATE
title: CRYPT_PROVIDER_SIGSTATE (wintrust.h)
description: Is used to communicate between policy providers and Wintrust.
helpviewer_keywords: ["*PCRYPT_PROVIDER_SIGSTATE","CRYPT_PROVIDER_SIGSTATE","CRYPT_PROVIDER_SIGSTATE structure [Security]","PCRYPT_PROVIDER_SIGSTATE","PCRYPT_PROVIDER_SIGSTATE structure pointer [Security]","security.crypt_provider_sigstate","wintrust/CRYPT_PROVIDER_SIGSTATE","wintrust/PCRYPT_PROVIDER_SIGSTATE"]
old-location: security\crypt_provider_sigstate.htm
tech.root: security
ms.assetid: B362A161-6B92-41B0-AE81-337EB42502D8
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_SIGSTATE, CRYPT_PROVIDER_SIGSTATE, CRYPT_PROVIDER_SIGSTATE structure [Security], PCRYPT_PROVIDER_SIGSTATE, PCRYPT_PROVIDER_SIGSTATE structure pointer [Security], security.crypt_provider_sigstate, wintrust/CRYPT_PROVIDER_SIGSTATE, wintrust/PCRYPT_PROVIDER_SIGSTATE'
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CRYPT_PROVIDER_SIGSTATE, *PCRYPT_PROVIDER_SIGSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_SIGSTATE
 - wintrust/_CRYPT_PROVIDER_SIGSTATE
 - PCRYPT_PROVIDER_SIGSTATE
 - wintrust/PCRYPT_PROVIDER_SIGSTATE
 - CRYPT_PROVIDER_SIGSTATE
 - wintrust/CRYPT_PROVIDER_SIGSTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_SIGSTATE
---

# CRYPT_PROVIDER_SIGSTATE structure


## -description

The <b>CRYPT_PROVIDER_SIGSTATE</b> structure is used to communicate between policy providers and Wintrust.

## -struct-fields

### -field cbStruct

Size, in bytes, of this structure.

### -field rhSecondarySigs

Pointer to an array of secondary signature handles.

### -field hPrimarySig

Handle of the primary signature.

### -field fFirstAttemptMade

Specifies whether the first attempt to verify a signature has been made.

### -field fNoMoreSigs

Specifies whether there exist further signatures that await verification.

### -field cSecondarySigs

Number of secondary signatures.

### -field dwCurrentIndex

Index of the signature currently being verified.

### -field fSupportMultiSig

Specifies whether the policy provider supports multiple signatures.

### -field dwCryptoPolicySupport

Identifies the portion of the policy provider that  supports cryptographic policy. This can be one of the following values:

<ul>
<li>WSS_OBJTRUST_SUPPORT</li>
<li>WSS_SIGTRUST_SUPPORT</li>
<li>WSS_CERTTRUST_SUPPORT</li>
</ul>

### -field iAttemptCount

### -field fCheckedSealing

### -field pSealingSignature

## -see-also

[WINTRUST_SIGNATURE_SETTINGS](/windows/desktop/api/wintrust/ns-wintrust-wintrust_signature_settings)