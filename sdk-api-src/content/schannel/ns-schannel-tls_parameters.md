---
UID: NS:schannel._TLS_PARAMETERS
title: TLS_PARAMETERS
ms.date: 11/4/2019
targetos: Windows
description: Indicates TLS parameter restrictions.
tech.root: security
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: schannel.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 1809 [desktop apps only]
req.target-type: Windows
req.typenames: TLS_PARAMETERS, *PTLS_PARAMETERS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - schannel.h
api_name:
 - _TLS_PARAMETERS
 - TLS_PARAMETERS
f1_keywords:
 - _TLS_PARAMETERS
 - schannel/_TLS_PARAMETERS
 - PTLS_PARAMETERS
 - schannel/PTLS_PARAMETERS
 - TLS_PARAMETERS
 - schannel/TLS_PARAMETERS
dev_langs:
 - c++
---

## -description

Indicates TLS parameter restrictions.

## -struct-fields

### -field cAlpnIds

The number of ALPN Ids in rgstrAlpnIds. 

Set to 0 if the following parameter restrictions apply regardless of the negotiated application protocol. It is an error to specify more than SCH_CRED_MAX_SUPPORTED_ALPN_IDS.

### -field rgstrAlpnIds

An array of ALPN IDs that the following parameters apply to. 

Set to NULL if parameter restrictions apply regardless of the negotiated application protocol.

### -field grbitDisabledProtocols

The bit string that represents the disabled protocols. 

Set to 0 to use system defaults. Schannel protocol flags are [documented here.](./ns-schannel-schannel_cred.md)

### -field cDisabledCrypto

The count of entries in the pDisabledCrypto array. It is an error to specify more than SCH_CRED_MAX_SUPPORTED_CRYPTO_SETTINGS.

### -field pDisabledCrypto

An array of pointers to the CRYPTO_SETTINGS structures that express disabled cryptographic settings.

### -field dwFlags

(*optional*) The flags to pass. 

When TLS_PARAMS_OPTIONAL is set, TLS_PARAMETERS will only be honored if they do not cause the server to terminate the handshake.

Otherwise, schannel may fail TLS handshakes in order to honor the TLS_PARAMETERS restrictions.

> [!NOTE]
> TLS_PARAMS_OPTIONAL is valid for server applications only. Must be zero otherwise.

## -remarks

## -see-also

[SCH_CREDENTIALS](ns-schannel-sch_credentials.md)

[CRYPTO_SETTINGS](ns-schannel-crypto_settings.md)