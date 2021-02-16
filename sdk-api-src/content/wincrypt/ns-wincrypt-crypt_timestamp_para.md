---
UID: NS:wincrypt._CRYPT_TIMESTAMP_PARA
title: CRYPT_TIMESTAMP_PARA (wincrypt.h)
description: Defines additional parameters for the time stamp request.
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_PARA","CRYPT_TIMESTAMP_PARA","CRYPT_TIMESTAMP_PARA structure [Security]","PCRYPT_TIMESTAMP_PARA","PCRYPT_TIMESTAMP_PARA structure pointer [Security]","security.crypt_timestamp_para","wincrypt/CRYPT_TIMESTAMP_PARA","wincrypt/PCRYPT_TIMESTAMP_PARA"]
old-location: security\crypt_timestamp_para.htm
tech.root: security
ms.assetid: 26a6e9d3-b35e-47ae-9cea-a37ca6297c28
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_PARA, CRYPT_TIMESTAMP_PARA, CRYPT_TIMESTAMP_PARA structure [Security], PCRYPT_TIMESTAMP_PARA, PCRYPT_TIMESTAMP_PARA structure pointer [Security], security.crypt_timestamp_para, wincrypt/CRYPT_TIMESTAMP_PARA, wincrypt/PCRYPT_TIMESTAMP_PARA'
req.header: wincrypt.h
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
req.typenames: CRYPT_TIMESTAMP_PARA, *PCRYPT_TIMESTAMP_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_PARA
 - wincrypt/_CRYPT_TIMESTAMP_PARA
 - PCRYPT_TIMESTAMP_PARA
 - wincrypt/PCRYPT_TIMESTAMP_PARA
 - CRYPT_TIMESTAMP_PARA
 - wincrypt/CRYPT_TIMESTAMP_PARA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_TIMESTAMP_PARA
---

# CRYPT_TIMESTAMP_PARA structure


## -description

The <b>CRYPT_TIMESTAMP_PARA</b> structure defines additional parameters for the time stamp request.

## -struct-fields

### -field pszTSAPolicyId

Optional. A pointer to a null-terminated character string that contains the Time Stamping Authority (TSA) policy under which the time stamp token
should be provided.

### -field fRequestCerts

A Boolean value that specifies whether the TSA must include the certificates
used to sign the time stamp token in the response .

### -field Nonce

Optional. A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available.

### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.

### -field rgExtension

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures that contain extension information that is passed in the request.