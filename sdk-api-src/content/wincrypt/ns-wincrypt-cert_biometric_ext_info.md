---
UID: NS:wincrypt._CERT_BIOMETRIC_EXT_INFO
title: CERT_BIOMETRIC_EXT_INFO (wincrypt.h)
description: Contains a set of biometric information.
helpviewer_keywords: ["*PCERT_BIOMETRIC_EXT_INFO","CERT_BIOMETRIC_EXT_INFO","CERT_BIOMETRIC_EXT_INFO structure [Security]","PCERT_BIOMETRIC_EXT_INFO","PCERT_BIOMETRIC_EXT_INFO structure pointer [Security]","security.cert_biometric_ext_info","wincrypt/CERT_BIOMETRIC_EXT_INFO","wincrypt/PCERT_BIOMETRIC_EXT_INFO"]
old-location: security\cert_biometric_ext_info.htm
tech.root: security
ms.assetid: b2a877e1-2be2-428c-bc47-ec5ce6cef7e6
ms.date: 12/05/2018
ms.keywords: '*PCERT_BIOMETRIC_EXT_INFO, CERT_BIOMETRIC_EXT_INFO, CERT_BIOMETRIC_EXT_INFO structure [Security], PCERT_BIOMETRIC_EXT_INFO, PCERT_BIOMETRIC_EXT_INFO structure pointer [Security], security.cert_biometric_ext_info, wincrypt/CERT_BIOMETRIC_EXT_INFO, wincrypt/PCERT_BIOMETRIC_EXT_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_BIOMETRIC_EXT_INFO, *PCERT_BIOMETRIC_EXT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_BIOMETRIC_EXT_INFO
 - wincrypt/_CERT_BIOMETRIC_EXT_INFO
 - PCERT_BIOMETRIC_EXT_INFO
 - wincrypt/PCERT_BIOMETRIC_EXT_INFO
 - CERT_BIOMETRIC_EXT_INFO
 - wincrypt/CERT_BIOMETRIC_EXT_INFO
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
 - CERT_BIOMETRIC_EXT_INFO
---

# CERT_BIOMETRIC_EXT_INFO structure


## -description

The <b>CERT_BIOMETRIC_EXT_INFO</b> structure contains a set of biometric information.

## -struct-fields

### -field cBiometricData

The number of elements in the <b>rgBiometricData</b> array.

### -field rgBiometricData

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_biometric_data">CERT_BIOMETRIC_DATA</a> structures that contain the biometric data. The <b>cBiometricData</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a>