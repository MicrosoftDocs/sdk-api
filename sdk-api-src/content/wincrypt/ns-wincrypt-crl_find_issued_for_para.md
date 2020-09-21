---
UID: NS:wincrypt._CRL_FIND_ISSUED_FOR_PARA
title: CRL_FIND_ISSUED_FOR_PARA (wincrypt.h)
description: Contains the certificate contexts of both a subject and a certificate issuer.
helpviewer_keywords: ["*PCRL_FIND_ISSUED_FOR_PARA","CRL_FIND_ISSUED_FOR_PARA","CRL_FIND_ISSUED_FOR_PARA structure [Security]","PCRL_FIND_ISSUED_FOR_PARA","PCRL_FIND_ISSUED_FOR_PARA structure pointer [Security]","_crypto2_crl_find_issued_for_para","security.crl_find_issued_for_para","wincrypt/CRL_FIND_ISSUED_FOR_PARA","wincrypt/PCRL_FIND_ISSUED_FOR_PARA"]
old-location: security\crl_find_issued_for_para.htm
tech.root: security
ms.assetid: a5c04859-00bb-4b7d-a98c-5b17bf0fa38a
ms.date: 12/05/2018
ms.keywords: '*PCRL_FIND_ISSUED_FOR_PARA, CRL_FIND_ISSUED_FOR_PARA, CRL_FIND_ISSUED_FOR_PARA structure [Security], PCRL_FIND_ISSUED_FOR_PARA, PCRL_FIND_ISSUED_FOR_PARA structure pointer [Security], _crypto2_crl_find_issued_for_para, security.crl_find_issued_for_para, wincrypt/CRL_FIND_ISSUED_FOR_PARA, wincrypt/PCRL_FIND_ISSUED_FOR_PARA'
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
req.typenames: CRL_FIND_ISSUED_FOR_PARA, *PCRL_FIND_ISSUED_FOR_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_FIND_ISSUED_FOR_PARA
 - wincrypt/_CRL_FIND_ISSUED_FOR_PARA
 - PCRL_FIND_ISSUED_FOR_PARA
 - wincrypt/PCRL_FIND_ISSUED_FOR_PARA
 - CRL_FIND_ISSUED_FOR_PARA
 - wincrypt/CRL_FIND_ISSUED_FOR_PARA
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
 - CRL_FIND_ISSUED_FOR_PARA
---

# CRL_FIND_ISSUED_FOR_PARA structure


## -description

The <b>CRL_FIND_ISSUED_FOR_PARA</b> structure contains the certificate contexts of both a subject and a certificate issuer. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcrlinstore">CertFindCRLInStore</a>.

## -struct-fields

### -field pSubjectCert

A pointer to a subject's certificate context.

### -field pIssuerCert

A pointer to a certificate issuer's certificate context.