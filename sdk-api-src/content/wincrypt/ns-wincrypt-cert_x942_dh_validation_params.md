---
UID: NS:wincrypt._CERT_X942_DH_VALIDATION_PARAMS
title: CERT_X942_DH_VALIDATION_PARAMS (wincrypt.h)
description: Optionally pointed to by a member of the CERT_X942_DH_PARAMETERS structure and contains additional seed information.
helpviewer_keywords: ["*PCERT_X942_DH_VALIDATION_PARAMS","CERT_942_DH_VALIDATION_PARAMS","CERT_942_DH_VALIDATION_PARAMS structure [Security]","CERT_X942_DH_VALIDATION_PARAMS","CERT_X942_DH_VALIDATION_PARAMS structure [Security]","PCERT942_DH_VALIDATION_PARAMS","PCERT942_DH_VALIDATION_PARAMS structure pointer [Security]","_crypto2_cert_x942_dh_validation_params","security.cert_x942_dh_validation_params","wincrypt/CERT_X942_DH_VALIDATION_PARAMS","wincrypt/PCERT942_DH_VALIDATION_PARAMS"]
old-location: security\cert_x942_dh_validation_params.htm
tech.root: security
ms.assetid: 26c367d5-c338-4db3-9973-ce21dcddf7ca
ms.date: 12/05/2018
ms.keywords: '*PCERT_X942_DH_VALIDATION_PARAMS, CERT_942_DH_VALIDATION_PARAMS, CERT_942_DH_VALIDATION_PARAMS structure [Security], CERT_X942_DH_VALIDATION_PARAMS, CERT_X942_DH_VALIDATION_PARAMS structure [Security], PCERT942_DH_VALIDATION_PARAMS, PCERT942_DH_VALIDATION_PARAMS structure pointer [Security], _crypto2_cert_x942_dh_validation_params, security.cert_x942_dh_validation_params, wincrypt/CERT_X942_DH_VALIDATION_PARAMS, wincrypt/PCERT942_DH_VALIDATION_PARAMS'
req.header: wincrypt.h
req.include-header: 
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
req.typenames: CERT_X942_DH_VALIDATION_PARAMS, *PCERT_X942_DH_VALIDATION_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_X942_DH_VALIDATION_PARAMS
 - wincrypt/_CERT_X942_DH_VALIDATION_PARAMS
 - PCERT_X942_DH_VALIDATION_PARAMS
 - wincrypt/PCERT_X942_DH_VALIDATION_PARAMS
 - CERT_X942_DH_VALIDATION_PARAMS
 - wincrypt/CERT_X942_DH_VALIDATION_PARAMS
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
 - CERT_942_DH_VALIDATION_PARAMS
---

# CERT_X942_DH_VALIDATION_PARAMS structure


## -description

The <b>CERT_X942_DH_VALIDATION_PARAMS</b> structure is optionally pointed to by a member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_x942_dh_parameters">CERT_X942_DH_PARAMETERS</a> structure and contains additional seed information.

## -struct-fields

### -field seed

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_UINT_BLOB</a> that contains an unsigned seed value.

### -field pgenCounter

A <b>DWORD</b> counter.