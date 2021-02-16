---
UID: NS:wincrypt._CERT_CRL_CONTEXT_PAIR
title: CERT_CRL_CONTEXT_PAIR (wincrypt.h)
description: The CERT_CRL_CONTEXT_PAIR structure contains a certificate context and an associated CRL context.
helpviewer_keywords: ["*PCERT_CRL_CONTEXT_PAIR","CERT_CRL_CONTEXT_PAIR","CERT_CRL_CONTEXT_PAIR structure [Security]","PCERT_CRL_CONTEXT_PAIR","PCERT_CRL_CONTEXT_PAIR structure pointer [Security]","_crypto2_cert_crl_context_pair","security.cert_crl_context_pair","wincrypt/CERT_CRL_CONTEXT_PAIR","wincrypt/PCERT_CRL_CONTEXT_PAIR"]
old-location: security\cert_crl_context_pair.htm
tech.root: security
ms.assetid: e88781f0-8474-47d3-8218-de95f7eadf04
ms.date: 12/05/2018
ms.keywords: '*PCERT_CRL_CONTEXT_PAIR, CERT_CRL_CONTEXT_PAIR, CERT_CRL_CONTEXT_PAIR structure [Security], PCERT_CRL_CONTEXT_PAIR, PCERT_CRL_CONTEXT_PAIR structure pointer [Security], _crypto2_cert_crl_context_pair, security.cert_crl_context_pair, wincrypt/CERT_CRL_CONTEXT_PAIR, wincrypt/PCERT_CRL_CONTEXT_PAIR'
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
req.typenames: CERT_CRL_CONTEXT_PAIR, *PCERT_CRL_CONTEXT_PAIR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CRL_CONTEXT_PAIR
 - wincrypt/_CERT_CRL_CONTEXT_PAIR
 - PCERT_CRL_CONTEXT_PAIR
 - wincrypt/PCERT_CRL_CONTEXT_PAIR
 - CERT_CRL_CONTEXT_PAIR
 - wincrypt/CERT_CRL_CONTEXT_PAIR
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
 - CERT_CRL_CONTEXT_PAIR
---

# CERT_CRL_CONTEXT_PAIR structure


## -description

The <b>CERT_CRL_CONTEXT_PAIR</b> structure contains a certificate context and an associated CRL context.

## -struct-fields

### -field pCertContext

A pointer to a certificate context.

### -field pCrlContext

A pointer to the certificate revocation list context.

