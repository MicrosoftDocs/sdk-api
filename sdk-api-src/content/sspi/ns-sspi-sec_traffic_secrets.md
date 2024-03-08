---
UID: NS:sspi._SEC_TRAFFIC_SECRETS
tech.root: security
title: SEC_TRAFFIC_SECRETS
ms.date: 07/20/2022
targetos: Windows
description: Contains the traffic secrets for a connection.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_TRAFFIC_SECRETS, *PSEC_TRAFFIC_SECRETS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_TRAFFIC_SECRETS
 - PSEC_TRAFFIC_SECRETS
 - SEC_TRAFFIC_SECRETS
f1_keywords:
 - _SEC_TRAFFIC_SECRETS
 - sspi/_SEC_TRAFFIC_SECRETS
 - PSEC_TRAFFIC_SECRETS
 - sspi/PSEC_TRAFFIC_SECRETS
 - SEC_TRAFFIC_SECRETS
 - sspi/SEC_TRAFFIC_SECRETS
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_TRAFFIC_SECRETS
---

## -description

Contains the traffic secrets for a connection.

## -struct-fields

### -field SymmetricAlgId

THe negotiated symmetric key algorithm (e.g. **BCRYPT_AES_ALGORITHM**).

### -field ChainingMode

The negotiated symmetric key algorithm chaining mode (e.g. **BCRYPT_CHAIN_MODE_GCM** or **BCRYPT_CHAIN_MODE_CCM**).

### -field HashAlgId

The negotiated hash algorithm (e.g. **BCRYPT_SHA256_ALGORITHM** or **BCRYPT_SHA384_ALGORITHM**).

### -field KeySize

They size (in bytes) of the symmetric key to derive from this traffic secret.

### -field IvSize

The size (in bytes) of the IV to derive from this traffic secret.

### -field MsgSequenceStart

The offset of the first byte of the TLS message sequence to be protected with a key derived from **TrafficSecret**. Use **0** to indicate the first byte of the buffer.

### -field MsgSequenceEnd

The offset of the last byte of the TLS message sequence to be protected with a key derived from **TrafficSecret**. Use **0** if the secret is for the encryption of application data or decryption of incoming records.

### -field TrafficSecretType

The type of traffic secret from the [TRAFFIC_SECRET_TYPE](ne-sspi-sec_traffic_secret_type.md) enumeration.

### -field TrafficSecretSize

The size (in bytes) of the traffic secret.

### -field TrafficSecret

Traffic secret of type **TrafficSecretType**, **TrafficSecretSize** bytes long, used to derive write key and IV for message protection.

## -remarks

## -see-also

[TRAFFIC_SECRET_TYPE](ne-sspi-sec_traffic_secret_type.md)
