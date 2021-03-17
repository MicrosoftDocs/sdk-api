---
UID: NS:wincrypt._CERT_REVOCATION_CRL_INFO
title: CERT_REVOCATION_CRL_INFO (wincrypt.h)
description: Contains information updated by a certificate revocation list (CRL) revocation type handler.
helpviewer_keywords: ["*PCERT_REVOCATION_CRL_INFO","CERT_REVOCATION_CRL_INFO","CERT_REVOCATION_CRL_INFO structure [Security]","PCERT_REVOCATION_CRL_INFO","PCERT_REVOCATION_CRL_INFO structure pointer [Security]","_crypto2_cert_revocation_crl_info","security.cert_revocation_crl_info","wincrypt/CERT_REVOCATION_CRL_INFO","wincrypt/PCERT_REVOCATION_CRL_INFO"]
old-location: security\cert_revocation_crl_info.htm
tech.root: security
ms.assetid: 069ff521-90fd-4de8-9b5c-045e44e87f75
ms.date: 12/05/2018
ms.keywords: '*PCERT_REVOCATION_CRL_INFO, CERT_REVOCATION_CRL_INFO, CERT_REVOCATION_CRL_INFO structure [Security], PCERT_REVOCATION_CRL_INFO, PCERT_REVOCATION_CRL_INFO structure pointer [Security], _crypto2_cert_revocation_crl_info, security.cert_revocation_crl_info, wincrypt/CERT_REVOCATION_CRL_INFO, wincrypt/PCERT_REVOCATION_CRL_INFO'
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
req.typenames: CERT_REVOCATION_CRL_INFO, *PCERT_REVOCATION_CRL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REVOCATION_CRL_INFO
 - wincrypt/_CERT_REVOCATION_CRL_INFO
 - PCERT_REVOCATION_CRL_INFO
 - wincrypt/PCERT_REVOCATION_CRL_INFO
 - CERT_REVOCATION_CRL_INFO
 - wincrypt/CERT_REVOCATION_CRL_INFO
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
 - CERT_REVOCATION_CRL_INFO
---

# CERT_REVOCATION_CRL_INFO structure


## -description

Contains information updated by a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) revocation type handler. The <b>CERT_REVOCATION_CRL_INFO</b> structure is used with both base and delta CRLs.

## -struct-fields

### -field cbSize

Size, in bytes, of the structure.

### -field pBaseCrlContext

### -field pDeltaCrlContext

### -field pCrlEntry

A pointer to an entry in either the base CRL or the delta CRL.

### -field fDeltaCrlEntry

<b>TRUE</b> if <b>pCrlEntry</b> points to an entry in the delta CRL. <b>FALSE</b> if <b>pCrlEntry</b> points to an entry in the base CRL.

### -field pBaseCRLContext

A pointer to a base CRL context.

### -field pDeltaCRLContext

A pointer to a delta CRL context.