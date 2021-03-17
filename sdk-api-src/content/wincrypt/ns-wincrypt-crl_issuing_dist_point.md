---
UID: NS:wincrypt._CRL_ISSUING_DIST_POINT
title: CRL_ISSUING_DIST_POINT (wincrypt.h)
description: Contains information about the kinds of certificates listed in a certificate revocation list (CRL).
helpviewer_keywords: ["*PCRL_ISSUING_DIST_POINT","CRL_ISSUING_DIST_POINT","CRL_ISSUING_DIST_POINT structure [Security]","PCRL_ISSUING_DIST_POINT","PCRL_ISSUING_DIST_POINT structure pointer [Security]","_crypto2_crl_issuing_dist_point","security.crl_issuing_dist_point","wincrypt/CRL_ISSUING_DIST_POINT","wincrypt/PCRL_ISSUING_DIST_POINT"]
old-location: security\crl_issuing_dist_point.htm
tech.root: security
ms.assetid: cdac9e96-5b26-4398-8863-16ea2c43f11e
ms.date: 12/05/2018
ms.keywords: '*PCRL_ISSUING_DIST_POINT, CRL_ISSUING_DIST_POINT, CRL_ISSUING_DIST_POINT structure [Security], PCRL_ISSUING_DIST_POINT, PCRL_ISSUING_DIST_POINT structure pointer [Security], _crypto2_crl_issuing_dist_point, security.crl_issuing_dist_point, wincrypt/CRL_ISSUING_DIST_POINT, wincrypt/PCRL_ISSUING_DIST_POINT'
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
req.typenames: CRL_ISSUING_DIST_POINT, *PCRL_ISSUING_DIST_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_ISSUING_DIST_POINT
 - wincrypt/_CRL_ISSUING_DIST_POINT
 - PCRL_ISSUING_DIST_POINT
 - wincrypt/PCRL_ISSUING_DIST_POINT
 - CRL_ISSUING_DIST_POINT
 - wincrypt/CRL_ISSUING_DIST_POINT
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
 - CRL_ISSUING_DIST_POINT
---

# CRL_ISSUING_DIST_POINT structure


## -description

The <b>CRL_ISSUING_DIST_POINT</b> structure contains information about the kinds of certificates listed in a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

## -struct-fields

### -field DistPointName

Optional 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point_name">CRL_DIST_POINT_NAME</a> member.

### -field fOnlyContainsUserCerts

<b>BOOL</b> flag. <b>TRUE</b> if only user certificates are contained in the CRL.

### -field fOnlyContainsCACerts

<b>BOOL</b> flag. <b>TRUE</b> if only CA certificates are contained in the CRL.

### -field OnlySomeReasonFlags

Optional 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> with bits indicating some reasons for certificate revocation.

### -field fIndirectCRL

<b>BOOL</b> flag. <b>TRUE</b> if this is an indirect CRL.