---
UID: NS:wincrypt._CERT_NAME_INFO
title: CERT_NAME_INFO (wincrypt.h)
description: Contains subject or issuer names.
helpviewer_keywords: ["*PCERT_NAME_INFO","CERT_NAME_INFO","CERT_NAME_INFO structure [Security]","PCERT_NAME_INFO","PCERT_NAME_INFO structure pointer [Security]","_crypto2_cert_name_info","security.cert_name_info","wincrypt/CERT_NAME_INFO","wincrypt/PCERT_NAME_INFO"]
old-location: security\cert_name_info.htm
tech.root: security
ms.assetid: 402d1051-d91a-4a79-96f6-10ed96a32d5c
ms.date: 12/05/2018
ms.keywords: '*PCERT_NAME_INFO, CERT_NAME_INFO, CERT_NAME_INFO structure [Security], PCERT_NAME_INFO, PCERT_NAME_INFO structure pointer [Security], _crypto2_cert_name_info, security.cert_name_info, wincrypt/CERT_NAME_INFO, wincrypt/PCERT_NAME_INFO'
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
req.typenames: CERT_NAME_INFO, *PCERT_NAME_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_NAME_INFO
 - wincrypt/_CERT_NAME_INFO
 - PCERT_NAME_INFO
 - wincrypt/PCERT_NAME_INFO
 - CERT_NAME_INFO
 - wincrypt/CERT_NAME_INFO
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
 - CERT_NAME_INFO
---

# CERT_NAME_INFO structure


## -description

The <b>CERT_NAME_INFO</b> structure contains subject or issuer names. The information is represented as an array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structures.

## -struct-fields

### -field cRDN

Number of elements in the <b>rgRDN</b> array.

### -field rgRDN

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>