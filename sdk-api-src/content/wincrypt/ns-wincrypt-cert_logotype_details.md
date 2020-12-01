---
UID: NS:wincrypt._CERT_LOGOTYPE_DETAILS
title: CERT_LOGOTYPE_DETAILS (wincrypt.h)
description: Contains additional information about a logotype.
helpviewer_keywords: ["*PCERT_LOGOTYPE_DETAILS","CERT_LOGOTYPE_DETAILS","CERT_LOGOTYPE_DETAILS structure [Security]","PCERT_LOGOTYPE_DETAILS","PCERT_LOGOTYPE_DETAILS structure pointer [Security]","security.cert_logotype_details","wincrypt/CERT_LOGOTYPE_DETAILS","wincrypt/PCERT_LOGOTYPE_DETAILS"]
old-location: security\cert_logotype_details.htm
tech.root: security
ms.assetid: cde420a8-c755-4c45-ab81-4897b08d9dd6
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS structure [Security], PCERT_LOGOTYPE_DETAILS, PCERT_LOGOTYPE_DETAILS structure pointer [Security], security.cert_logotype_details, wincrypt/CERT_LOGOTYPE_DETAILS, wincrypt/PCERT_LOGOTYPE_DETAILS'
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
req.typenames: CERT_LOGOTYPE_DETAILS, *PCERT_LOGOTYPE_DETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_DETAILS
 - wincrypt/_CERT_LOGOTYPE_DETAILS
 - PCERT_LOGOTYPE_DETAILS
 - wincrypt/PCERT_LOGOTYPE_DETAILS
 - CERT_LOGOTYPE_DETAILS
 - wincrypt/CERT_LOGOTYPE_DETAILS
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
 - CERT_LOGOTYPE_DETAILS
---

# CERT_LOGOTYPE_DETAILS structure


## -description

The <b>CERT_LOGOTYPE_DETAILS</b> structure contains additional information about a logotype.

## -struct-fields

### -field pwszMimeType

The address of a null-terminated Unicode string that contains the Multipurpose Internet Mail Extensions (MIME) type of the logotype.

### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.

### -field rgHashedUrl

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structures that contain the hashed URLs of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_audio">CERT_LOGOTYPE_AUDIO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_image">CERT_LOGOTYPE_IMAGE</a>