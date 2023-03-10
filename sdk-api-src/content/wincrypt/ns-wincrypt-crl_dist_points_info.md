---
UID: NS:wincrypt._CRL_DIST_POINTS_INFO
title: CRL_DIST_POINTS_INFO (wincrypt.h)
description: Contains a list of certificate revocation list (CRL) distribution points a certificate user can reference to determine whether the certificate has been revoked.
helpviewer_keywords: ["*PCRL_DIST_POINTS_INFO","CRL_DIST_POINTS_INFO","CRL_DIST_POINTS_INFO structure [Security]","PCRL_DIST_POINTS_INFO","PCRL_DIST_POINTS_INFO structure pointer [Security]","_crypto2_crl_dist_points_info","security.crl_dist_points_info","wincrypt/CRL_DIST_POINTS_INFO","wincrypt/PCRL_DIST_POINTS_INFO"]
old-location: security\crl_dist_points_info.htm
tech.root: security
ms.assetid: cc0fe49c-80ab-42d8-9756-a6d6b885761e
ms.date: 12/05/2018
ms.keywords: '*PCRL_DIST_POINTS_INFO, CRL_DIST_POINTS_INFO, CRL_DIST_POINTS_INFO structure [Security], PCRL_DIST_POINTS_INFO, PCRL_DIST_POINTS_INFO structure pointer [Security], _crypto2_crl_dist_points_info, security.crl_dist_points_info, wincrypt/CRL_DIST_POINTS_INFO, wincrypt/PCRL_DIST_POINTS_INFO'
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
req.typenames: CRL_DIST_POINTS_INFO, *PCRL_DIST_POINTS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_DIST_POINTS_INFO
 - wincrypt/_CRL_DIST_POINTS_INFO
 - PCRL_DIST_POINTS_INFO
 - wincrypt/PCRL_DIST_POINTS_INFO
 - CRL_DIST_POINTS_INFO
 - wincrypt/CRL_DIST_POINTS_INFO
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
 - CRL_DIST_POINTS_INFO
---

# CRL_DIST_POINTS_INFO structure


## -description

The <b>CRL_DIST_POINTS_INFO</b> structure contains a list of <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution points a certificate user can reference to determine whether the certificate has been revoked.

## -struct-fields

### -field cDistPoint

Number of elements in the <b>rgDistPoint</b> member array.

### -field rgDistPoint

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point">CRL_DIST_POINT</a> structures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point">CRL_DIST_POINT</a>