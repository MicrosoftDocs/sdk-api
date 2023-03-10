---
UID: NS:wincrypt._CERT_LOGOTYPE_REFERENCE
title: CERT_LOGOTYPE_REFERENCE (wincrypt.h)
description: Contains logotype reference information.
helpviewer_keywords: ["*PCERT_LOGOTYPE_REFERENCE","CERT_LOGOTYPE_REFERENCE","CERT_LOGOTYPE_REFERENCE structure [Security]","PCERT_LOGOTYPE_REFERENCE","PCERT_LOGOTYPE_REFERENCE structure pointer [Security]","security.cert_logotype_reference","wincrypt/CERT_LOGOTYPE_REFERENCE","wincrypt/PCERT_LOGOTYPE_REFERENCE"]
old-location: security\cert_logotype_reference.htm
tech.root: security
ms.assetid: 22e6492e-afc2-4160-ad6c-0b65265eafeb
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_REFERENCE, CERT_LOGOTYPE_REFERENCE, CERT_LOGOTYPE_REFERENCE structure [Security], PCERT_LOGOTYPE_REFERENCE, PCERT_LOGOTYPE_REFERENCE structure pointer [Security], security.cert_logotype_reference, wincrypt/CERT_LOGOTYPE_REFERENCE, wincrypt/PCERT_LOGOTYPE_REFERENCE'
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
req.typenames: CERT_LOGOTYPE_REFERENCE, *PCERT_LOGOTYPE_REFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_REFERENCE
 - wincrypt/_CERT_LOGOTYPE_REFERENCE
 - PCERT_LOGOTYPE_REFERENCE
 - wincrypt/PCERT_LOGOTYPE_REFERENCE
 - CERT_LOGOTYPE_REFERENCE
 - wincrypt/CERT_LOGOTYPE_REFERENCE
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
 - CERT_LOGOTYPE_REFERENCE
---

# CERT_LOGOTYPE_REFERENCE structure


## -description

The <b>CERT_LOGOTYPE_REFERENCE</b> structure contains logotype reference information.

## -struct-fields

### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.

### -field rgHashedUrl

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structures that contain the hashed URL of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.